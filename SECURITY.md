# Field Preflight Security Policy

Operator: Qing Sun, operating under the Quiet Trellis brand.
Security contact: sqingdmwc@gmail.com.
Effective date: October 27, 2026.

## App scope and access

Field Preflight for Jira provides read-only field dependency evidence and review
guidance for Jira Cloud administrators. It does not modify, delete or migrate
Jira fields, configuration or work items. Results reflect available evidence,
the caller's permissions and collection limits; they do not authorize a field
change or guarantee discovery of every dependency.

The app uses Atlassian Forge Custom UI and the Forge bridge to request Jira data
as the signed-in caller on the installed site. An administrator display condition
and a runtime Jira administrator permission check restrict entry. The app does
not bypass Jira permissions or ask customers for passwords, API tokens or shared
service credentials. Access is based on Jira administrator status, not a permanent
allowlist of one person's email address.

## Data handling and technical controls

Reports, optional imports and comparisons are processed in browser-session
memory. The app has no publisher-operated report database, remote application
backend or external analytics/logging pipeline. Requests use an allowlisted GET
surface with bounded pagination, request counts, timeouts and input parsing.
Imported JSON is subject to size and structural validation; imported text is
not executed as code or rendered as arbitrary HTML.

Configuration, filter-owner metadata and JQL can contain personal or confidential
information. Users may explicitly download JSON reports to their own devices.
These downloads persist until users delete them; uninstalling the app does not
remove them. Protect exports and avoid sharing unredacted reports. Atlassian's
platform processing, logging, encryption and service policies apply separately;
this policy does not claim that platform services perform no logging or that all
data remains in a particular region.

See the [Privacy Policy](https://github.com/sqingdmw/field-preflight-docs/blob/main/PRIVACY.md)
for support correspondence, local exports and privacy requests. Support email is
separate from app telemetry. Do not send sensitive diagnostic attachments unless
the necessary content and appropriate transfer method have first been agreed.

## Reporting a security concern

Email sqingdmwc@gmail.com with subject "Field Preflight security report".
Include the affected app operation/version if known, a minimal reproduction,
potential impact and a way to contact you. Use synthetic examples where possible.
Never send passwords, API tokens, verification codes, another tenant's data or
an unredacted Automation export/report.

Test only systems and information you are authorized to access. Do not disrupt
services, obtain other users' data or perform destructive testing. Contact us
privately so we can coordinate investigation and disclosure. This reporting
channel does not grant testing access, legal safe harbor or a bounty entitlement.

## Vulnerability maintenance

The operator will review security reports and relevant dependency advisories,
assess whether released versions are affected, and maintain records of findings
and remediation. Dependency review forms part of release preparation. Security
fixes will be prioritized according to impact and the applicable
[Atlassian Security Bug Fix Policy](https://developer.atlassian.com/platform/marketplace/security-bugfix-policy/),
including assigned remediation due dates and communications with Atlassian.
Blocked remediation will be communicated rather than treated as an automatic
extension or waiver.

The released toolchain includes reviewed self-maintained dependency patches.
Their maintenance remains the operator's responsibility; upstream advisory
withdrawal and previous scan results are not vendor endorsement or proof of
ongoing absence of vulnerabilities. Findings that affect customers will be
handled through the applicable vulnerability and incident processes.

## Incident response

For suspected app compromise or unauthorized exposure of end-user data, the
operator will assess the impact, take appropriate containment measures,
coordinate with Atlassian under its
[incident management guidelines](https://developer.atlassian.com/platform/marketplace/app-security-incident-management-guidelines/),
and notify affected customers as required by applicable law, agreements and
platform requirements. Available facts will be reported without waiting for a
complete investigation. Updates and corrective actions will follow as more
information becomes available. Containment can require temporarily restricting
app availability in coordination with Atlassian.

This policy does not promise 24/7 staffed support, a contractual acknowledgement
or resolution SLA, a bug bounty, independent penetration testing, or ISO/SOC
certification. These limits do not replace applicable incident-notification or
vulnerability-remediation obligations. No blanket regulatory compliance or
guarantee of security is claimed.

## Policy updates

Material changes to app security or data handling will be reflected in dated
public documentation and the relevant Marketplace disclosures. The operator
remains responsible for the accuracy of those disclosures.
