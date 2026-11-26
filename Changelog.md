# Changes to Windows11-CIS-Audit

## CIS Benchmark v3.0.0
## November 2026 - QA fixes

- run_audit.ps1 reads audit policy by subcategory GUID from auditpol /backup, any display language (addresses https://github.com/ansible-lockdown/Windows-11-CIS/issues/45) - Thank you @exu-g
- collector_targets.json carries the subcategory GUID
- 17.3.1 title suffix is the benchmark name PNP Activity
- 18.9.25.2 asserts LAPS PasswordExpirationProtectionEnabled
- run_audit.ps1 falls back to the registry when CIM lookups fail after an admin rename
- run_audit.ps1 warns when the firewall profiles cannot be read
- 5.39 and 18.9.4.2 titles: PDF line-wrap hyphen spacing removed
- LICENSE company name Quantum Sky
- 18.4.7 gated on win11cis_netbt_nodetype being P-node, as the role
- .gitignore secret and QA artifact patterns
- README resource counts updated
- goss.yml renamed syver.yml
- skip reasons in the skip-reason attribute
- run_audit.ps1 requires syver 0.16.0, validated on 0.21.0

## September 2026 - BitLocker profile, RDVDenyWriteAccess and NIST meta

- 18.10.92.4.4 asserts SetAllowOptionalContent
- 18.10.92.4.4 asserts the stray AllowOptionalContent value is absent
- 18.10.9.3.14 asserts RDVDenyWriteAccess under SYSTEM\CurrentControlSet\Policies\Microsoft\FVE
- 18.10.9.3.14 asserts the stray SOFTWARE\Policies\Microsoft\FVE value is absent
- malformed NIST800-53R5 meta removed from 10 controls
- README: win11cis_bitlocker documented as a role gate

## September 2026 - standalone and domain joined hosts

- 30 controls no longer gated on win11cis_domain_joined; only LAPS remains domain gated
- README: stale BitLocker standalone note removed

## September 2026 - NIST mappings

- NIST800-53R5 meta added to 358 controls
- controls with no NIST tag in the role carry no NIST field

## September 2026 - 2.3.11.6

- 2.3.11.6 asserts ForceLogoffWhenHourExpire, not LanManServer EnableForcedLogOff
- 2.3.11.6 asserted on hosts that are not domain joined only
- Collector captures ForceLogoffWhenHourExpire
- Section 1 account policy and 2.3.11.6 reported as skipped on a domain joined host, with the reason in meta.skip_reason

## 1.0.0 based on CIS Benchmark v3.0.0

- Initial release - beta, pending feedback. Please raise an issue or reach us on
  Discord with anything it gets wrong, reports unexpectedly, or misses
