# Insight451 Calculated Fields Repo


* [Funnel Stage](#funnel-stage)
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
    ISDATE(STR([Milestone Created Date]))
THEN "1-Suspect"
ELSEIF (ISNULL([Milestone Admit Date]) AND 
    ISNULL([Milestone Application Submit Date]) AND 
    ISNULL([Milestone Application Start Date]) AND
    ISNULL([Milestone Deposit Date]))
    AND
    ISDATE(STR([Milestone Prospect Date]))
THEN "2-Prospect"
ELSEIF (ISNULL([Milestone Admit Date]) AND
    ISNULL([Milestone Deposit Date]))
    AND
    (ISDATE(STR([Milestone Application Start Date])) 
        OR ISDATE(STR([Milestone Application Complete Date])) 
        OR ISDATE(STR([Milestone Application Submit Date]))) 
THEN "3-Applicants"
ELSEIF (ISNULL([Milestone Deposit Date])) AND 
    ISDATE(STR([Milestone Admit Date]))
THEN "4-Admits"
ELSEIF
    ISDATE(STR([Milestone Deposit Date]))
THEN "5-Deposit"
ELSEIF
    ISDATE(STR([Milestone Enroll Date]))
THEN "6-Enrolled"
ELSEIF
    ISDATE(STR([Milestone Withdraw Date]))
THEN "Other:Withdrawn/Melt"
ELSEIF
    ISDATE(STR([Milestone Waitlist Date]))
THEN "Other:Waitlist"
ELSE "Other:NA"
END
```


# Other

TBD
