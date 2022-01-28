---
name: Comment Template
about: Describe this issue template's purpose here.
title: ''
labels: ''
assignees: ''

---

[ ] Removal of access from Accessshub for

[ ] IAM resources
[ ] SoftLayer resources (if applicable)
[ ] GHE orgs - access hub removes team access but not org access
[ ] New Relic - remove access to accounts (CD Public: 1783376, CD Dedicated: 2228819, ...) Access to NR is controlled via AH Application: ccs-newrelic
[ ] Removal of Accesses not managed through AccessHUB

[ ] Vault - Owners defined here to raise access removal request following guidleinelines documented Vault Remove Members Runbook
[ ] SOS - work with security focal to remove from portal; ** NEED VALIDATION ** ( Should it be this link )
[ ] Thycotic - Remove accesses not controlled using AccessHub to secrets in Thycotic . ** NEED VALIDATION ** Link not updated **
[ ] PagerDuty - Remove from CD team: Bluemix DevOps Services OTC; remove from Insights team: CD Insights ** NEED VALIDATION - How to Link **
[ ] ServiceNow - Refer ServiceNow Runbook
[ ] ASoC - ask in #sos-asoc to remove user from "IBM DevOps Services" group
[ ] Slack channels -Remove from private slack channels
[ ] Box folders -Remove from Box folders (Example WW CD Team , DevOps Insights Dev , SRE-devops-services, Any squad specific folders )
[ ] Aha!  - when the intranet ID is removed from BluePages, the user should be removed from Aha. If you want to be sure, you can contact an admin in #bigblue-aha-liaison Slack channel to remove from the account.
[ ] Remove from GitHub (public) Repos: Open toolchain templates ** NEED VALIDATION **
[ ] Removal of access to Shared accounts or credentials, in which case immediately trigger their rotation/change

[ ] Revoke/rotate IAM keys the user had access to {do users have any user level keys they use to access services?
[ ] How do we revoke them? Do we care only about IAM keys used to access prod resources or all their IAM keys?  If an employee leaves the company they can/should all be revoked, but if they change roles, what should we do?  TODO: check with IAM team what happens to keys in a federated account when an employee leaves the company.}
[ ] Revoke/rotate IAM serviceIDs the user had access to
[ ] do users have an user level serviceIDs they use to access services?  There shouldn't be any of these.
[ ] Rotate secrets to data stores/services the employee had access to in Vault (TODO: need link)
[ ] currently, anyone with Vault access can see all secrets because of the way we use it; this makes it painful to have to rotate keys when someone leaves the team. List of people with Access can be seen here
[ ] Rotate secrets to data stores/services the employee had access to in KeyProtect (not applicable as of May 2020, will be soon)
