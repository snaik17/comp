---
name: Offboarding:Transfer
about: 'Offboarding : Transfer'
title: Offboarding of <name of employee>
labels: ''
assignees: ''

---

CISO Ticket

 ###  Service Team : Access To Be Revoked Checklist (Offboarding)
 - [ ] Agree on which permissions the transferred individual needs to temporarily maintain, if any (e.g., needed for completing transfer of activities from the old job role). Please consider that any access that is maintained for transfer-related activities is only allowed for needed period of time, after which, New Manager needs to trigger the revoke on AccessHub or other relevant access management/account tools.

 - [ ] Document in the issue all the permissions that are being retained by the transferred individual specifically for transfer-related activities. Update the Transition end-date field in the Information section with a planned date by which all the transition-related activities will be completed and the related permissions will be revoked.

| Application        | Permissions           | Revoked       | Date Revoked| 
| ------------------ |:---------------------:| -------------:| -----------:|
| GHE                |                       |     Y/N       |             |
| IAM                |                       |     Y/N       |             |
| Softlayer          |                       |     Y/N       |             |
| New Relic          |                       |     Y/N       |             |
| SOS                |                       |     Y/N       |             |
| Thycotic           |                       |     Y/N       |             |
| Vault              |                       |     Y/N       |             |
| Pagerduty          |                       |     Y/N       |             |
| Slack              |                       |     Y/N       |             |
| Box                |                       |     Y/N       |             |
| Other              |                       |     Y/N       |             |



- [ ] Process all the event-driven CBN triggered for the individual by all the applicable Account Management systems, which will be directed to New Manager, within 15 days. For AccessHub New Manager can leverage “consulting” feature to request input from Old Manager. Refer to the AccessHub documentation.

- [ ] Promptly revoke ANY access that is no longer required for the new job role, including accesses not managed through Account Manag ement systems (e.g. IBM box, github, private slack channel, etc.)

-[ ] Assess if the transferred individual had access to any shared accounts or credentials, in which case immediately trigger their rotation/change, and document in this issue the list of impacted accounts/credentials.

   - [ ] Revoke & Rotate  **IAM keys** and **IAM serviceIDs** Check items user had access to by checking the [IAM Inventory Link](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/iam-credentials.csv) 

      - **IAM Service ID** : Update owner/rotator to new owner/rotator in [IAM Config ](https://github.ibm.com/org-ids/key-rotation/tree/master/config) and raise pull request. Daily automation will run and update the [Inventory](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/)
     
      - **IAM key** :  - Update the following the ) and also update owner/rotator in the file [here](https://github.ibm.com/org-ids/key-rotation/blob/master/functionalID-user-mapping.yaml) and also update [Link](https://github.ibm.com/org-ids/key-rotation/tree/master/runbook#api-keys-ownership

   - [ ] Revoke & Rotate  **non-IAM keys** : Check items user had access to by checking
       the [non-IAM Inventory](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/non-iam-credentials.csv) 
   
      - Update owner/rotator in [here](https://github.ibm.com/org-ids/key-rotation/blob/master/config-non-iam/credentials.yaml) and raise pull request. Daily automation will run and update the [non-IAM Inventory ](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/non-iam-credentials.csv) 
   
  
   - [ ] Rotate secrets to data stores/services the employee had access to in Vault
       - List of people with Access can be seen [here](https://ibm.ent.box.com/file/344444043206?s=t3qnek4rzidylcp3yt4pe01xx5bjhgzb)
         If person User - revoke access
         If Person is Owner in Vault - all keys must be rotated. (*** HOW ?**)

- [ ] - If the individual worked on Financial Services Cloud:
        Report transfer of that individual to their upline manager within two (2) days of the formal transfer date. Capture screenshot of email.

- [ ] If the individual worked on HIPAA regulated environment:
    Perform the required offboarding steps in the HIPAA checklist 
    (Acknowledgement: When you no longer require production access, you must complete WCP offboarding procedures and confirm that no customer PHI existed on your workstation or all customer PHI has been removed by an IBM approved disposal tool.)

 ------
### Off-Boarding: Change of Manager/Department:
**Verify employee access has been removed within 7 days**

  - **Off-Boarding: Change of Manager/Department**
      No explicit action is needed. Access Hub syncs with Enterprise directory every 27 minutes. Continuous CBN ('EventTriggered') is set up by default and runs automatically when a user’s department or manager changes. AccessHub will batch the required re-validations until Friday of the respective week. Revalidation is initiated once a week (Friday) with all changes that happened since the last Continuous CBN was launched. Perform the following activities to confirm access is removed:
     1. Run "My Application EventTriggered CBN" report to make sure Continuous CBN has been triggered. Once manager revokes access, verify employee access is eventually removed
     2. Run "My Application User Data" report to make sure employee is no longer listed in Access Hub. Take screen-shots of first and last page and also download report.
     3. Run the command (and redirect output to file) "ibmcloud account users' to list the users on the IAM side to make sure employee is not longer listed. Take screenshot with date.
     4. Record the following output (from steps 2 and 3 above) in the off-boarding git issue:
        a) screenshots with dates 
        b) attach xlsx report and output of command

### Off-Boarding: Leaving IBM:
**Verify employee access has been removed within 24 hrs**
**Verify that all the privilidged creds which employee have access to have been changed ASAP after resignation** 


 - [AccessHub](https://ibm.idaccesshub.com/ECM/) - review ALL accesses for the employee in AccessHub (before transfer to new manager) and revoke accesses no longer needed.  This will cover access to production and development resources in bmdevops (prod), DevOps.Admin (EU prod), devops.eu.org (EU dev) and bmdevops.dev (dev) accounts. This will also cover Insights Jenkins server and any WhiteWater Github Domains controlled via AccessHub.
  
  - **Off-Boarding: Leaving IBM**
     No explicit action is needed to remove the employee. Access Hub syncs with Enterprise directory every 27 minutes and initiates a Delete task. Perform the following activities to confirm access is removed:
      1. Run "My Application Leaver’s" report to make sure employee is listed
      1. Run "My Application User Data" report to make sure employee is no longer listed in Access Hub. Take screen-shots of first and last page and also download report. 
      1. Run the command (and redirect output to file) to list the users on the IAM side ‘ibmcloud account users’ to make sure employee is not longer listed. Take screenshot with date.
      1. Record the following output (from steps 2 and 3 above) in the off-boarding git issue:
        a) screenshots with dates, and 
        b) attach xlsx report and output of command  
        
***Note Managers Please check that the leavng employee is not be part of current CBN process***
