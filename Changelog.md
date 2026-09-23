# Changes to Windows11-CIS-Audit

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

## 1.0.0 based on CIS Benchmark v3.0.0

- Initial release - beta, pending feedback. Please raise an issue or reach us on
  Discord with anything it gets wrong, reports unexpectedly, or misses
