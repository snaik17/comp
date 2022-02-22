---
name: Offboarding:Transfer
about: 'Offboarding : Transfer'
title: Offboarding of <name of employee>
labels: ''
assignees: ''

---

Refer the [Offboarding Runbook](https://github.ibm.com/org-ids/compliance/blob/master/runbooks/access-control/Offboarding.md)

Link to [CISO Ticket](https://github.ibm.com/ibmcloud/ciso-compliance-offboarding/issues) :

-----

 -    **Removal of access from [Accessshub](https://ibm.idaccesshub.com/ECMv6/request/requestHome)** ([Details](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub.md)) 
      - Open [AccessHUB Home page](https://ibm.idaccesshub.com/ECMv6/request/requestHome).
      - Click Request or Manage Access for Others (to delete an account for someone who is transfering out of your team) 
      -  Search for the user, then click user & select Manage
      - Next you will see a list of applications member has access to , select and click-on Delete.
      - Confirm by entering reason for removal - "User is leaving CD team and no longer needs access to CD resources", then click-on Remove 
      - Resource List :
          - [ ] [IAM resources](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub.md)
        - [ ] [SoftLayer resources](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub-SL.md) 
        - [ ] [GHE orgs](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub-GHE.md) 
        - [ ] [New Relic](https://synthetics.newrelic.com) - remove access to accounts (CD Public: [1783376](https://synthetics.newrelic.com/accounts/1783376), CD Dedicated: [2228819](https://synthetics.newrelic.com/accounts/2228819), ...) AH Application: `ccs-newrelic`
        - [ ] [SOS](https://w3.sos.ibm.com/) - [Accesshub Removal link](https://pages.github.ibm.com/SOSTeam/SOS-Docs/idmgt/accesshub/Delete-account/#steps-to-delete-account) and then work with security focal to remove from [portal](https://w3.sos.ibm.com/inventory.nsf/compliance_portal.xsp?c_code=ridos); 
        -  [ ] [Thycotic](https://pimconsole.sos.ibm.com/) - [Link]( https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/Thycotic.md#preconditions) 

  -  **Removal of Accesses not managed through AccessHUB**
      - [ ]  Vault - Owners defined [here](https://ibm.ent.box.com/notes/344444043206) to raise access removal request following guidleinelines documented [Vault Remove Members Runbook](https://pages.github.ibm.com/vault-as-a-service/vault/onboarding/remove-members.html)
      - [ ] [PagerDuty](https://ibm.pagerduty.com/) - Remove from CD team: Bluemix DevOps Services OTC; remove from Insights team: CD Insights [Link](https://w3.ibm.com/w3publisher/pagerduty/getting-started/offboarding)
      - [ ] [ServiceNow](https://watson.service-now.com/) -  Refer [ ServiceNow Runbook ](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/ServiceNow-Access.md#removing-users)
      - [ ] [ASoC](https://cloud.appscan.com/AsoCUI/serviceui/main/myapps/oneapp/f8fca2ac-7671-e811-9423-002590ac753d/scans) - ask in `#sos-asoc` to remove user from "IBM DevOps Services" group
      - [ ] Slack - Remove from private slack channels
      - [ ] Box folders - Remove from  Box folders (Example [WW CD Team](https://ibm.ent.box.com/folder/30409987383?s),DevOps Insights Dev, SRE-devops-services, Any squad specific folders ) Follow [this](https://support.box.com/hc/en-us/articles/360044196273-Managing-Collaborators#transferfolderowner) for Transfer of Ownership incase needed
      - [ ] [Aha! ](https://secure.aha.io/) -  when the intranet ID is removed from BluePages, the user should be removed from Aha. If you want to be sure, you can contact an admin in #bigblue-aha-liaison Slack channel to remove from the account. 
      - [ ] Remove from GitHub (public) Repos: [Open toolchain templates](https://github.com/open-toolchain/) 

In case access was not revoked by transfer date and needed to be maintained temporarily beyond last day in team ( transition period) - mention those specific ones permissions in CISO ticket . These need to be removed at the end of transition period and CBN triggered by New manager. 

-[ ] Assess if the transferred individual had access to any shared accounts or credentials, in which case immediately trigger their rotation/change, and document in this issue the list of impacted accounts/credentials.

   - [ ] Revoke & Rotate  **IAM keys** and **IAM serviceIDs** Check items user had access to by checking the [IAM Inventory Link](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/iam-credentials.csv) 
      - **IAM Service ID** : Update owner/rotator to new owner/rotator in [IAM Config ](https://github.ibm.com/org-ids/key-rotation/tree/master/config) and raise pull request. Daily automation will run and update the [Inventory](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/)    
      - **IAM key** :  - Follow the [Link](https://github.ibm.com/org-ids/key-rotation/tree/master/) and update owner/rotator in the file [here](https://github.ibm.com/org-ids/key-rotation/blob/master/functionalID-user-mapping.yaml)
   - [ ] Revoke & Rotate  **non-IAM keys** : Check items user had access to by checking
       the [non-IAM Inventory](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/non-iam-credentials.csv) 
      - Update owner/rotator in [here](https://github.ibm.com/org-ids/key-rotation/blob/master/config-non-iam/credentials.yaml) and raise pull request. Daily automation will run and update the [non-IAM Inventory ](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/non-iam-credentials.csv)    
   - [ ] Rotate secrets to data stores/services the employee had access to in Vault
       - List of people with Access can be seen [here](https://ibm.ent.box.com/file/344444043206?s=t3qnek4rzidylcp3yt4pe01xx5bjhgzb)
         If person is User in Vault - revoke access.
         If Person is Owner in Vault - all keys must be rotated. 
   - [ ] Rotate secrets to data stores/services the employee had access to in KeyProtect
    
- [ ]  If the individual worked on Financial Services Cloud:
        Report transfer of that individual to their upline manager within two (2) days of the formal transfer date. Capture screenshot of email.

- [ ] If the individual worked on HIPAA regulated environment:
    Perform the required offboarding steps in the HIPAA checklist 
    (Acknowledgement: When you no longer require production access, you must complete WCP offboarding procedures and confirm that no customer PHI existed on your workstation or all customer PHI has been removed by an IBM approved disposal tool.)
