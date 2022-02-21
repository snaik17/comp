---
name: Bug report
about: Offboarding Ticket Template
title: Offboarding for <name >
labels: ''
assignees: ''

---

---
# Employee Offboard Checklist
Guidelines are provided in [WCP Doc](https://pages.github.ibm.com/ibmcloud/Security/guidance/offboarding_procedure.html)

## Personnel Offboard Runbook

The IBM cloud offboarding process covers IBM employees and contractors and refers to both :
1. [Transfers of personnel](https://pages.github.ibm.com/ibmcloud/Security/guidance/personnel-onboarding-offboarding.html#personnel-transfer)


2. [Termination of personnel leaving the company](https://pages.github.ibm.com/ibmcloud/Security/guidance/personnel-onboarding-offboarding.html#personnel-termination)


An employee’s functional manager is responsible for offboarding his/her employees and the issue for Offboarding is maintained in the [CISO Compliance Offboarding](https://github.ibm.com/ibmcloud/ciso-compliance-offboarding/issues)
- Incase manager does not have access to the [CISO Compliance Offboarding](https://github.ibm.com/ibmcloud/ciso-compliance-offboarding/issues), request access via 
[#cloud-offboarding-ask channel](https://ibm-cloudplatform.slack.com/archives/C02UTTT9Q05)

[CISO Offboarding FAQ](https://github.ibm.com/ibmcloud/ciso-compliance-offboarding/blob/master/faq.md)

## Create (for termination) or Edit (for transfer) Offboarding issue (Effective 24 Jan 2022) 

1) **Personnel Transfer** 
   - A git issue is automatically created in the [CISO Compliance Offboarding](https://github.ibm.com/ibmcloud/ciso-compliance-offboarding/issues) and asssigned to  old   manager. Responsbilty of the old managers  to document their transition plan within 2 days of the transfer date in the GHE issue, and update the ticket to document the completion of the transition period and provide required evidence in the ticket and close it following guidance given under [Personnel Transfer](https://pages.github.ibm.com/ibmcloud/Security/guidance/personnel-onboarding-offboarding.html#personnel-transfer)


2) **Personnel Termination** 
   - The manager has to manually create a new git issue using the [leavers template](https://github.ibm.com/ibmcloud/ciso-compliance-offboarding/issues/new?template=offboarding-leaver-template.md) in the [CISO Compliance Offboarding Repo](https://github.ibm.com/ibmcloud/ciso-compliance-offboarding/issues) following  guidance given under [Personal Termination](https://pages.github.ibm.com/ibmcloud/Security/guidance/personnel-onboarding-offboarding.html#personnel-termination).

* Since the above tickets capture high level info, we will provide additional detailed offboarding information (and evidence) by appending information to the git issue from the section [ Service Team : Acess To Be Revoked Checklist (Leaver/Transfer as appropriate)] in a comment.

Guidance on updating checkboxes in the CISO Offboarding Issue: 
- Check the box for those done, leave unchecked for those that are not done and for those that don’t apply, and describe it in a comment to the issue.

-----


 ###  Service Team : Acess To Be Revoked Checklist (Leaver)
  
- **Terminate/revoke any authenticators/credentials associated with that individual on the last day worked**

  -  **Removal of access from [Accessshub](https://ibm.idaccesshub.com/ECMv6/request/requestHome)** ([Details](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub.md))
     - [ ] [IAM resources](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub.md)
     - [ ] [SoftLayer resources](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub-SL.md) 
     - [ ] [GHE orgs](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub-GHE.md) - access hub removes team access but not org access
     - [ ] [New Relic](https://synthetics.newrelic.com) - remove access to accounts (CD Public: [1783376](https://synthetics.newrelic.com/accounts/1783376), CD Dedicated: [2228819](https://synthetics.newrelic.com/accounts/2228819), ...) AH Application: `ccs-newrelic`
     - [ ] [SOS](https://w3.sos.ibm.com/) - [Accesshub Removal link](https://pages.github.ibm.com/SOSTeam/SOS-Docs/idmgt/accesshub/Delete-account/#steps-to-delete-account) and then work with security focal to remove from [portal](https://w3.sos.ibm.com/inventory.nsf/compliance_portal.xsp?c_code=ridos); 
     - [ ] [Thycotic](https://pimconsole.sos.ibm.com/) - [Link]( https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/Thycotic.md#preconditions) (*** HOW ?**)

  -  **Removal of Accesses not managed through AccessHUB**
      - [ ]  Vault - Owners defined [here](https://ibm.ent.box.com/notes/344444043206) to raise access removal request following guidleinelines documented [Vault Remove Members Runbook](https://pages.github.ibm.com/vault-as-a-service/vault/onboarding/remove-members.html)
      - [ ] [PagerDuty](https://ibm.pagerduty.com/) - Remove from CD team: Bluemix DevOps Services OTC; remove from Insights team: CD Insights ** NEED VALIDATION - How to Link  ** 
      - [ ] [ServiceNow](https://watson.service-now.com/) -  Refer [ ServiceNow Runbook ](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/ServiceNow-Access.md#removing-users)
      - [ ] [ASoC](https://cloud.appscan.com/AsoCUI/serviceui/main/myapps/oneapp/f8fca2ac-7671-e811-9423-002590ac753d/scans) - ask in `#sos-asoc` to remove user from "IBM DevOps Services" group
      - [ ] Slack channels -Remove from private slack channels
      - [ ] Box folders -Remove from  Box folders (Example [WW CD Team](https://ibm.ent.box.com/folder/30409987383?s) , DevOps Insights Dev , SRE-devops-services, Any squad specific folders ) Follow [this](https://support.box.com/hc/en-us/articles/360044196273-Managing-Collaborators#transferfolderowner) for Transfer of Ownership incase needed
      - [ ] [Aha! ](https://secure.aha.io/) -  when the intranet ID is removed from BluePages, the user should be removed from Aha. If you want to be sure, you can contact an admin in #bigblue-aha-liaison Slack channel to remove from the account. 
      - [ ] Remove from GitHub (public) Repos: [Open toolchain templates](https://github.com/open-toolchain/)  ** NEED VALIDATION **
 

-  **Assess if the leaver had access to any shared accounts or credentials, in which case immediately trigger their rotation/change, and document in this issue the list of impacted accounts/credentials.**

   - [ ] Revoke & Rotate  **IAM keys** and **IAM serviceIDs** Check items user had access to by checking the [IAM Inventory Link](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/iam-credentials.csv) 

      - **IAM Service ID** : Update owner/rotator to new owner/rotator in [IAM Config ](https://github.ibm.com/org-ids/key-rotation/tree/master/config) and raise pull request. Daily automation will run and update the [Inventory](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/)
     
      - **IAM key** :  - Follow the [Link](https://github.ibm.com/org-ids/key-rotation/tree/master/) and update owner/rotator in the file [here](https://github.ibm.com/org-ids/key-rotation/blob/master/functionalID-user-mapping.yaml)

   - [ ] Revoke & Rotate  **non-IAM keys** : Check items user had access to by checking
       the [non-IAM Inventory](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/non-iam-credentials.csv) 
   
      - Update owner/rotator in [here](https://github.ibm.com/org-ids/key-rotation/blob/master/config-non-iam/credentials.yaml) and raise pull request. Daily automation will run and update the [non-IAM Inventory ](https://github.ibm.com/org-ids/key-rotation/blob/master/credential-inventory/non-iam-credentials.csv) 
   
  
   - [ ] Rotate secrets to data stores/services the employee had access to in Vault
       - List of people with Access can be seen [here](https://ibm.ent.box.com/file/344444043206?s=t3qnek4rzidylcp3yt4pe01xx5bjhgzb)
         If person User - revoke access
         If Person is Owner in Vault - all keys must be rotated. (*** HOW ?**)

   - [ ] Rotate secrets to data stores/services the employee had access to in KeyProtect (*** HOW ?**)

- **Make sure the leaver cleans up any personal cloud resources (i.e., personal cloud account and any related cloud resource)**

  - [ ] Follow this [runbook] () 
- **If the individual worked on Financial Services Cloud, report termination of that individual to their upline manager on the last day worked.**
   - [ ] Send email to Upline manager and capture screenshot.

- **Retain access to organizational information and information system-related property (e.g. hardware authentication tokens, keys, identification cards, etc.) and list in this issue the items that have been returned by the individual leaving IBM.** 
  - [ ] ID Card
  - [ ] Laptop
  - [ ] Hardware authentication Token : Yubi Keys etc
  - [ ] AMEX Card
