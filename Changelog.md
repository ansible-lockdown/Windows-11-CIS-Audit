# Changes to Windows11-CIS-Audit

## October 2026 - registry locations

- 18.9.26.2 asserts LAPS PasswordExpirationProtectionEnabled
- 18.9.27.2 asserts RunAsPPL under SOFTWARE\Policies\Microsoft\Windows\System
- 18.4.4 asserts the Wow6432Node EnableCertPaddingCheck value
- run_audit.ps1 falls back to the registry when CIM lookups fail after an admin rename
- run_audit.ps1 warns when the firewall profiles cannot be read
- 18.10.3.1 asserts DisableAPISamping under AppCompat
- 18.10.94.4.1 asserts SetAllowOptionalContent

## September 2026 - BitLocker profile and RDVDenyWriteAccess

- 18.10.10.3.14 asserts RDVDenyWriteAccess under SYSTEM\CurrentControlSet\Policies\Microsoft\FVE
- 18.10.10.3.14 asserts the stray SOFTWARE\Policies\Microsoft\FVE value is absent
- README: win11cis_bitlocker documented as a role gate

## September 2026 - standalone hosts

- 25 controls no longer gated on win11cis_domain_joined; only LAPS remains domain gated
- README: stale BitLocker standalone note removed

## September 2026 - NIST mappings

- NIST800-53R5 meta on 357 controls, generated from the role tags

## September 2026 - 2.3.11.5 and domain members

- 2.3.11.5 asserts ForceLogoffWhenHourExpire, not LanManServer EnableForcedLogOff
- Collector captures ForceLogoffWhenHourExpire
- Section 1 account policy and 2.3.11.5 reported as skipped on a domain joined host, with the reason in meta.skip_reason

## 2.0.0 based on CIS Benchmark v5.1.0

- Regenerated in full from Private-Windows-11-CIS at benchmark v5.1.0
- 535 of 535 controls asserted
- 47 retired controls removed, 42 new controls added, 253 renumbered
- benchmark_version and run_audit.ps1 BenchmarkVer now read v5.1.0

## CIS Benchmark v3.0.0 - September 2026 - BitLocker profile, RDVDenyWriteAccess and NIST meta

- 18.10.9.3.14 asserts RDVDenyWriteAccess under SYSTEM\CurrentControlSet\Policies\Microsoft\FVE
- 18.10.9.3.14 asserts the stray SOFTWARE\Policies\Microsoft\FVE value is absent
- malformed NIST800-53R5 meta removed from 10 controls
- README: win11cis_bitlocker documented as a role gate

## CIS Benchmark v3.0.0 - September 2026 - standalone and domain joined hosts

- 30 controls no longer gated on win11cis_domain_joined; only LAPS remains domain gated
- README: stale BitLocker standalone note removed

## CIS Benchmark v3.0.0 - September 2026 - NIST mappings

- NIST800-53R5 meta added to 358 controls
- controls with no NIST tag in the role carry no NIST field

## CIS Benchmark v3.0.0 - September 2026 - 2.3.11.6

- 2.3.11.6 asserts ForceLogoffWhenHourExpire, not LanManServer EnableForcedLogOff
- 2.3.11.6 asserted on hosts that are not domain joined only
- Collector captures ForceLogoffWhenHourExpire
- Section 1 account policy and 2.3.11.6 reported as skipped on a domain joined host, with the reason in meta.skip_reason

## 1.0.0 based on CIS Benchmark v3.0.0

- Initial release - beta, pending feedback. Please raise an issue or reach us on
  Discord with anything it gets wrong, reports unexpectedly, or misses
