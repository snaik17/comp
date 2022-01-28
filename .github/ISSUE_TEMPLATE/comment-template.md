---
name: Comment Template
about: Describe this issue template's purpose here.
title: ''
labels: ''
assignees: ''

---

-  [ ] Removal of access from [Accessshub](https://ibm.idaccesshub.com/ECMv6/request/requestHome) for 
   - [ ] [IAM resources](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub.md)
   - [ ] [SoftLayer resources](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub-SL.md) (if applicable)
   - [ ] [GHE orgs](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub-GHE.md) - access hub removes team access but not org access
   - [ ] [New Relic](https://synthetics.newrelic.com) - remove access to accounts (CD Public: [1783376](https://synthetics.newrelic.com/accounts/1783376), CD Dedicated: [2228819](https://synthetics.newrelic.com/accounts/2228819), ...)  Access to NR is controlled via AH Application: `ccs-newrelic`
 


- [ ]  Removal of Accesses not managed through AccessHUB  
   - [ ]  Vault - Owners defined [here](https://ibm.ent.box.com/notes/344444043206) to raise access removal request following guidleinelines documented [Vault Remove Members Runbook](https://pages.github.ibm.com/vault-as-a-service/vault/onboarding/remove-members.html)
   - [ ] [SOS](https://w3.sos.ibm.com/) - work with security focal to remove from [portal](https://w3.sos.ibm.com/inventory.nsf/compliance_portal.xsp?c_code=ridos); ** NEED VALIDATION **
 ( Should it be this [link](https://pages.github.ibm.com/SOSTeam/SOS-Docs/idmgt/accesshub/Delete-account/#steps-to-delete-account) )
   - [ ] [Thycotic](https://pimconsole.sos.ibm.com/) - Remove accesses not controlled using AccessHub to secrets in Thycotic .  ** NEED VALIDATION ** [Link]( https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/Thycotic.md#preconditions) not updated **
   - [ ] [PagerDuty](https://ibm.pagerduty.com/) - Remove from CD team: Bluemix DevOps Services OTC; remove from Insights team: CD Insights ** NEED VALIDATION - How to Link  ** 
   - [ ] [ServiceNow](https://watson.service-now.com/) -  Refer [ ServiceNow Runbook ](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/ServiceNow-Access.md#removing-users)
   - [ ] [ASoC](https://cloud.appscan.com/AsoCUI/serviceui/main/myapps/oneapp/f8fca2ac-7671-e811-9423-002590ac753d/scans) - ask in `#sos-asoc` to remove user from "IBM DevOps Services" group
   - [ ] Slack channels -Remove from private slack channels
   - [ ] Box folders -Remove from  Box folders (Example [WW CD Team](https://ibm.ent.box.com/folder/30409987383?s) , DevOps Insights Dev , SRE-devops-services, Any squad specific folders )
   - [ ] [Aha! ](https://secure.aha.io/) -  when the intranet ID is removed from BluePages, the user should be removed from Aha. If you want to be sure, you can contact an admin in #bigblue-aha-liaison Slack channel to remove from the account. 
   - [ ] Remove from GitHub (public) Repos: [Open toolchain templates](https://github.com/open-toolchain/)  ** NEED VALIDATION **
 
- [ ] Removal of access to Shared accounts or credentials, in which case immediately trigger their rotation/change
  - [ ] Revoke/rotate IAM keys the user had access to {do users have any user level keys they use to access services? 
  - [ ] How do we revoke them? Do we care only about IAM keys used to access prod resources or all their IAM keys?  If an employee leaves the company they can/should all be revoked, but if they change roles, what should we do?  TODO: check with IAM team what happens to keys in a federated account when an employee leaves the company.}
  - [ ] Revoke/rotate IAM serviceIDs the user had access to 
  - [ ] do users have an user level serviceIDs they use to access services?  There shouldn't be any of these.
 - [ ] Rotate secrets to data stores/services the employee had access to in Vault (TODO: need link)
   - [ ] currently, anyone with Vault access can see all secrets because of the way we use it; this makes it painful to have to rotate keys when someone leaves the team. List of people with Access can be seen [here](https://ibm.ent.box.com/file/344444043206?s=t3qnek4rzidylcp3yt4pe01xx5bjhgzb)
 - [ ] Rotate secrets to data stores/services the employee had access to in KeyProtect (not applicable as of May 2020, will be soon)
