# Insight451 Calculated Fields Repo


* [Funnel Stage](#funnel-stage)
* [ActiveTerm](#active-term)
* [Other](#other)


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
IF [Funnel] == "1-Suspect" OR  [Funnel] == "2-Prospect"
THEN [Intended Term Name]
ELSEIF  [Funnel] == "3-Applicants"
THEN [Term Name]
ELSE "NA"
END
```

# Other
TBD
```
Code here

```
