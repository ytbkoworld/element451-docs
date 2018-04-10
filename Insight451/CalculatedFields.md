# Insight451 Calculated Fields Repo
The following variables use a "left-join" from element_user + element_applications.  Then, we can compute:  

* [Funnel Stage](#funnel-stage)
* [ActiveTerm](#active-term)
* [Year to Year](#yoy)
* [Engagement Score](#engagement-score)


# Funnel Stage 

Computes recruitment funnel from milestones.
```
IF (ISNULL([Milestone Admit Date]) AND 
    ISNULL([Milestone Application Submit Date]) AND 
    ISNULL([Milestone Application Start Date]) AND
    ISNULL([Milestone Deposit Date]) AND 
    ISNULL([Milestone Prospect Date]))
    AND
    not ISNULL([Milestone Created Date])
THEN "1-Suspect"
ELSEIF (ISNULL([Milestone Admit Date]) AND 
    ISNULL([Milestone Application Submit Date]) AND 
    ISNULL([Milestone Application Start Date]) AND
    ISNULL([Milestone Deposit Date]))
    AND
    not ISNULL([Milestone Prospect Date])
THEN "2-Prospect"
ELSEIF (ISNULL([Milestone Admit Date]) AND
    ISNULL([Milestone Deposit Date]))
    AND
    (not ISNULL([Milestone Application Start Date]) 
        OR not ISNULL([Milestone Application Complete Date]) 
        OR not ISNULL([Milestone Application Submit Date])) 
THEN "3-Applicants"
ELSEIF (ISNULL([Milestone Deposit Date])) AND 
    not ISNULL([Milestone Admit Date])
THEN "4-Admits"
ELSEIF
    not ISNULL([Milestone Deposit Date])
THEN "5-Deposit"
ELSEIF
    not ISNULL([Milestone Enroll Date])
THEN "6-Enrolled"
ELSEIF
    not ISNULL([Milestone Withdraw Date])
THEN "Other:Withdrawn/Melt"
ELSEIF
    not ISNULL([Milestone Waitlist Date])
THEN "Other:Waitlist"
ELSE "Other:NA"
END
```

# Active Term
Assigns a term
```
IFNULL([Term Name],[Intended Term Name])
```

# YoY%
Return % change from year-to-year
```
sum([Is In Current Year])/sum([Is In Prior Year])-1

```
[Is In Current Year]
```
IF [Submitted At] > [Sem start date (mm/dd)] AND  [Submitted At] <= [YoY (mm/dd) (copy)] AND [Term Name] == [Current Year Term ]
THEN 1
Else 0
END
```

[Is In Prior Year]
```
IF [Submitted At] > DATEADD('year',-1,[Sem start date (mm/dd)]) AND  
[Submitted At] <= DATEADD('year',-1,[YoY (mm/dd) (copy)])
AND [Term Name] == [Prior Year Term]
THEN 1
Else 0
END
```

# Engagement Score
Computes digital engagement score from email, SMS, forms, and logins
```

#Trait Computation = "engagementScore"
engagementScore = emailScore+smsScore+formsSaved+userLogin

emailScore = #emailClicked/#emailDelivered
smsScore = #smsClicked/#smsDelivered

formsSaved = 	if (#total_forms/#formSaved ==0) then 0
				if (#total_forms/#formSaved <.25) then 0.0625
				if (#total_forms/#formSaved <.5) then 0.125
				if (#total_forms/#formSaved <.75) then 0.1875
				if (#total_forms/#formSaved >=1) then 0.25
				

userLogin= 	if (#dayssincelastlogin<=10) then 0.25
			if (#dayssincelastlogin>=30) then 0.10
			if (#dayssincelastlogin>30) then 0.05
			

#Validation/Truncation
if emailScore >.25 then emailScore == 0.25
if smsScore >.25 then smsScore == 0.25
if emailUnsubscribed == TRUE then emailScore == 0

#Labeling
If engagementScore ==0 then "DORMANT"
If engagementScore <0.33 then "LURKER"
If engagementScore >=0.33 then "FAN"

```
