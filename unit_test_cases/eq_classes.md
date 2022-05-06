## Equivalence Classes

### Notes:

 - The intermediary nodes do not form equivalence classes because e.g. whether a workflow is valid is entirely determined by the equivalence classes listed below!
 - Are termination states an input condition?

### Input Conditions:

#### Syntax and spelling

0. There are yaml syntax errors.
1. There aren't yaml syntax errors.
3. All tags are valide.
4. At least one tag is invalid (e.g. "owenr" instead of owner, "attachments" for Slack)

#### Owner

0. VALID The workflow's owner is engineering.
1. VALID The workflow's owner is a current January employee.
2. INVALID The workflow's owner is invalid (mispelled / former employee).

#### Collaborators

3. VALID The workflow's valid collaborators are specified.
4. INVALID The workflow's invalid collaborators are specified.
5. VALID The workflow's collaborators are not specified.

#### SLAs

12. VALID The workflow specifies a failure SLA.
13. INVALID The workflow doesn't specify a failure SLA.
14. VALID The workflow specifies a success SLA.
15. VALID The workflow doesn't specify a success SLA.

#### Failure Channels

6. VALID The workflow specifies Asana as a failure channel. 
6. INVALID The workflow doesn't specify Asana as a failure channel. 
7. VALID The workflow specifies Pagerduty as a failure channel. 
7. VALID The workflow doesn't specity Pagerduty as a failure channel. 
8. INVALID The workflow specifies an invalid failure channel (Slack, email, Monday).

#### Success Channels

9. VALID The workflow specifies Asana as a success channel. 
9. VALID The workflow doesn't specify Asana as a success channel. 
10. VALID The workflow specifies Slack as a success channel. 
10. VALID The workflow doesn't specify Slack as a success channel. 
11. INVALID The workflow specifies an invalid success channel (Pagerduty, email, Monday).

#### Additional messaging for Asana

16. VALID The workflow specifies additional messaging for Asana failure.
17. VALID The workflow doesn't specify additional messaging for Asana failure.
18. VALID The workflow specifies additional messaging for Asana success.
19. VALID The workflow doesn't specify additional messaging for Asana success.

#### Additional projects for Asana

20. VALID The workflow specifies additional projects for Asana failure.
21. VALID The workflow doesn't specify additional projects for Asana failure.
22. VALID The workflow specifies additional projects for Asana success.
23. VALID The workflow doesn't specify additional projects for Asana success.

#### Additional attachments for Asana

24. VALID The workflow specifies additional attachments for Asana failure.
25. VALID The workflow doesn't specify additional attachments for Asana failure.
26. VALID The workflow specifies additional attachments for Asana success.
27. VALID The workflow doesn't specify additional attachments for Asana success.

#### Additional parameters

28. INVALID An additional parameter is added to Pagerduty failure.
29. INVALID An additional parameter is added to Slack success.
30. VALID No additional parameters are added to non-Asana channels.

#### Triggers (???)

31. VALID The workflow is triggered in Automat Live.
32. VALID The workflow is triggered via cron.
33. VALID The workflow is triggered via "Retry Last Task" button.

#### Comment: is this even an input condition?
#### Termination (this can trigger if e.g. Postgres goes down - should we include Postgres???)

34. INVALID the workflow terminates with a status of "failed".
35. VALID the workflow terminates with a status of "succeeded".

### Output Conditions

?

### Test cases 

?



