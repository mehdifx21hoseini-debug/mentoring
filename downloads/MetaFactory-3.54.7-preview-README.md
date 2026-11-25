# MetaFactory 3.54.7 preview

## Findings from the user's comparison
The 3.54.6 report contains a live chart-review process MT4-03_review-02, PID13284, while the primary MT4-03 process exited. The old row and report header counted only primaries, so running0 was misleading. The same observer produced verified live reports on MT4-04 and MT4-05; that does not establish a general observer failure. Review survival narrows the issue to the primary/live environment or startup context, but does not isolate the EA alone or prove account authentication in the review window.

## Correct per-type visibility
- A row with review copies shows two compact lines: Live open/closed and Review open. Running review never implies a fresh live report. Existing error detail remains in the status tooltip.
- Open filter includes a student whose review copy is open. Footer Open terminals and Close open count actual primary+review processes; the Open tab counts matching student rows.
- Open/Show on the main row continues to target the live primary, as requested. Show chart review appears in the row's menu when a review is open.
- System check reports primary/live and review counts separately, includes review processes in the total/resource summary, and adds bounded review PID/path/current-run native-login evidence. A native login acknowledgement is labelled separately from a live-report heartbeat. Standalone Diagnose includes managed review copies too.

## Explicit rebuild for an affected report copy
Right-click MT4-03 or use its three-dot menu and choose Rebuild report copy. Confirmation names that one copy/account. It requires a saved investor account and a closed primary; a review copy can remain open. No rebuild happens automatically.

- A fresh terminal is staged from a separate installed broker terminal, not from the failing copy. Staging uses the primary's own drive. The original folder is retained under _MTManager/repair-backups/MT4-03/<UTC-and-unique-id>; original native account cache, profiles, charts and other files remain in that backup. Expiring generated startup credential INIs are cleaned before backup.
- The fresh folder replaces only that primary at the same path. MetaFactory account/password/note/report records and review copy directory/ownership stay saved. After commit, the selected primary launches in live mode. Fresh broker history may need to synchronize again.
- Running-primary checks are repeated before replacement; the original executable is guarded during directory moves on Windows. Linked repair roots and unexpected copy paths are rejected. Original files are restored if copying/cancellation/replacement fails before commit; backups are never deleted.
- Stop cancels preparation. If commit already finished, fresh files and the old backup stay retained and further launch stops. Normal application close during rebuilding requests safe cancellation and asks the user to close again once it finishes. Forced process termination/power loss can require manual restoration from the retained backup path; this is not a cross-directory filesystem transaction.
- This provides a controlled clean-environment repair/test. The specific native cause of MT4-03's code0 exit is still unproven until tested on Windows; no native cure is claimed from Linux tests.

## Install and use
Close MetaFactory and install MetaFactory-Setup-3.54.7-preview.exe. Review-only state will now display correctly. For the failing MT4-03 primary, choose Rebuild report copy from its row menu, confirm, and wait for completion. Chart review may remain open. If the fresh live primary still exits, send System check and troubleshooting again; it will distinguish both roles and include rebuilt-terminal evidence.

## Validation
Built against Microsoft .NET Framework4.5 reference assemblies. Full logic:2377 passed,0 failed (one pre-existing Python/Unix chart retry check skipped). Additional rebuild filesystem checks:12 passed, covering backup contents, old chart/cache preservation, fresh staging, review ownership, running-primary rejection, source failure, cancellation including after original-to-backup rename, rollback and owned-stage cleanup. Previous close-audit/startup cleanup checks:14 passed. In English/Persian at normal and simulated125% scale:78 launch/role-state/selection/close checks,30 progress/stop checks,82 table/name/note/hover checks passed per run. Real harmless sleeper processes verify review-only row/Open filter/report counts and separate close scopes. Application close cancellation and exact clicked-row targeting were checked. Actual review-only row screenshot inspected. Installer payload/version/resources, ZIP integrity and actual remote downloads verified before delivery. No Windows directory-lock, native broker, repair effectiveness or MetaEditor execution claim is made from these Linux tests. Native financial sources and report calculations are unchanged from3.54.6.
