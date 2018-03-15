# Insight451 Calculated Fields Repo
The following variables use a "left-join" from element_user + element_applications.  Then, we can compute:  

* [Funnel Stage](#funnel-stage)
* [ActiveTerm](#active-term)
* [Year to Year %](#yoy%)


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
