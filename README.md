# Field Preflight for Jira

Read-only custom-field dependency review for Jira Cloud administrators, by
Quiet Trellis.

## Free Marketplace Submission

The app has been submitted for a free Marketplace listing and is awaiting
Atlassian approval and publisher verification. It is not yet an approved public
listing. The pre-submission installation-link trial was completed; do not assume
that link distribution remains available after submission. Contact
sqingdmwc@gmail.com for availability. Your own Jira subscription and permissions
still apply; no developer token or CLI is required for app use.

A site administrator reviews Atlassian's installation consent and installs on
their authorized Jira site. Open Jira Apps > Field Preflight using a Jira
administrator account. The app reads evidence as the signed-in user. It never
changes, migrates, trashes or deletes Jira fields or work items.

## Run A Review

1. Search for and select a custom field by its name and ID.
2. Optionally restrict searchable project scope using project keys.
3. Optionally select your own Jira Automation JSON export.
4. Select Run preflight. The proposed retirement is analysis only.
5. Review field-purpose guidance, observed risk, coverage and reason breakdown.
6. Expand Evidence and Review Plan entries; check Coverage for collection limits.
7. Download the JSON report to preserve the result outside the browser session.

## Understand The Result

Observed risk and coverage are independent. Review Required needs human
disposition; LOW observed risk is not approval to retire a field. Verified means
verified within the stated collector scope, not universal completeness.

EXACT references identify configured field references, not proof that a workflow
is assigned or currently used. Name matches remain candidates. Boards reached
through a matching filter are indirect associations, not direct field-use proof.
Visible populated-value counts can exclude restricted or archived work items.
Project scope does not prove that global configuration is limited to those projects.
Suggested reviewers are not assigned owners.

Automation is not automatically scanned using a rule-management API. Optional
exports are parsed in the browser; missing exports are Not provided. Confirm
currency and scope with the rule owner. Omitted rules cannot be discovered.

Comparison accepts a compatible report or reviewed session baseline. Confirm
same-site provenance and matching scope when prompted. Missing evidence or a
changed count does not prove that a dependency was resolved.

## Limits And Troubleshooting

Private filters, restricted work items, app-private configuration, dashboards and
external integrations may be inaccessible or unsupported. Effective project and
workflow/screen-scheme inventories are not comprehensively enumerated. Errors and
limits remain unknowns, not zero usage. No enterprise-wide completeness is promised.

The scan budget is 150 bridge calls/90 seconds, with a 15-second per-request
timeout and 20-page collector cap. Automation files are limited to 20 MiB and
baseline reports to 5 MiB; structural checks also apply. Cancellation stops new
calls/waiting but may not cancel an already submitted request. Atlassian platform
quotas and rate limits still apply.

For access failures, check Jira administrator rights, installation consent and
site app-access rules. A 403 is unknown, not proof of no dependency. Reloading or
closing discards unsaved session state. Protect downloaded files and do not send
unredacted reports to support. Before real changes, obtain owner review and follow
your backup/change-management procedures. This app never authorizes deletion.

## Policies And Support

- [Privacy policy](PRIVACY.md)
- [User terms](TERMS.md)
- [Support and security reports](SUPPORT.md)
- [Security policy](SECURITY.md)

This repository contains public documentation only, not application source code,
tenant reports, credentials or internal support records.
