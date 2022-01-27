---
name: Offboarding
about: Describe this issue template's purpose here.
title: 'Offboarding Request for <name of Employee , Surname > '
labels: ''
assignees: ''

---

[Offboarding document] (https://github.ibm.com/org-ids/compliance/blob/master/runbooks/access-control/Offboarding.md)

CISO Ticket Number : <Link to CISO Ticket>
Type : Leaving IBM  / Transfer to another Unit

Badge , Yubikey , Laptop Return is tracked in main CISO issue .

Incase employee did not have access , please mark NA

Project Details
- [] Revoke [Vault access] (https://ibm.ent.box.com/notes/344444043206) 
  - Note: [runbook](https://pages.github.ibm.com/vault-as-a-service/vault/onboarding/remove-members.html) for this - an owner needs to submit this request
- [] Remove access to [Thycotic](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/Thycotic.md#preconditions) 
- [] SOS ID: work with security focal to remove from [portal](https://w3.sos.ibm.com/inventory.nsf/compliance_portal.xsp?c_code=ridos) - N/A
- [] PagerDuty - N/A
- [] [ServiceNow](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/ServiceNow-Access.md#removing-users) 
- [] NewRelic
  -  access to NR is controlled via AH Application `ccs-newrelic`
- [] Revoke/rotate IAM keys the user had access to - N/A
  - [] transfer ownership of keys in inventory - N/A
- [] Revoke/rotate IAM serviceIDs the user had access to - N/A 
  - [] transfer ownership of serviceIDs in inventory - N/A
- [] Rotate secrets to data stores/services the employee had access to in KeyProtect - N/A, no access to regional CRK (per chat with Christophe)
- [] Remove from [ASoC](https://cloud.appscan.com/AsoCUI/serviceui/main/myapps/oneapp/f8fca2ac-7671-e811-9423-002590ac753d/scans) - ask in `#sos-asoc` to remove user from "IBM DevOps Services" group
- [] Remove from private Slack channels 
- [] Remove from project Box folders
  - WW CD Team, DevOps Insights Dev, SRE-devops-services, any squad specific folders
- [] Remove from GitHub (public) repos 

- [] Validate AccessHub removal 
  - [] [IAM resources](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub.md)
  - [] [SoftLayer resources](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub-SL.md) (if applicable)
  - [] Remove from [CD GHE orgs](https://github.ibm.com/org-ids/otc-developer-runbooks/blob/master/common/AccessHub-GHE.md) - access hub removes team access but not org access

- [] Return Laptop 
- [] Return badge 
- [] Yubikey
