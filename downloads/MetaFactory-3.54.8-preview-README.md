# MetaFactory 3.54.8 preview

## Repair access-denied follow-up
The screenshot shows Access to E:\MetaTrader\MT4-03 is denied during rebuild, not evidence that the yellow memory advisory caused the failure. In3.54.7 the repair routine kept terminal.exe open while moving its containing directory. That can interfere with Windows folder movement; the source handle is no longer opened/retained during directory rename. This removes a concrete interference risk, but the screenshot alone cannot distinguish it from an external lock, folder attributes or ACL restrictions.

- Retains repeated primary-process checks, investor-account requirement, explicit confirmation, same-drive staging, backups, rollback, and safe normal-app-close/cancel behavior.
- Retries only Win32 access/sharing/lock codes5/32/33, at most4 attempts with100/200/400ms waits. Each attempt checks stop and primary process state. It does not terminate a lock holder, change ACL/ownership, request elevation or alter UAC.
- A bounded last-repair record reports copy, phase, exact Win32 code when available, HRESULT, original/backup/stage paths and existence/attribute query results. Generic managed errors are not assigned a guessed Windows code. GUI failure names the phase/code and preserves prior-data location accurately. System check and standalone Diagnose include the record.
- A failed fresh placement restores the old directory where possible. A failed rollback explicitly retains and identifies the backup. No native Windows cure is claimed from Linux tests.

## Requested report-time layout
- The last-report age is again below the Today / No trades today text, including at full-width layout.
- The previous Last report column remains an empty reserved column for the account information the user will specify later. Its header, cell content and tooltip are blank; clicking its blank header does not sort. Existing compact-window hiding behavior remains. No proposed account metrics are filled in yet.
- Timestamp data, financial calculations, reporting/native EAs, review/live launch behavior and per-role status/counts are unchanged.

## Install and next check
Close MetaFactory and install MetaFactory-Setup-3.54.8-preview.exe. On MT4-03, choose Rebuild report copy again while its primary is closed; chart review may remain open. The old folder is retained under _MTManager/repair-backups. If access is still denied, send Support → System check and troubleshooting; the new record identifies the failed operation/code. Native MT4-03 live-exit diagnosis is still pending until the rebuild succeeds and the fresh live primary is tested.

## Verification
Built against Microsoft .NET Framework4.5 reference assemblies. Rebuild filesystem suite:18 passed, including exclusive access to the source executable during injected moves (no retained self-handle), transient sharing retry, bounded permanent access denial with phase/code, commit failure rollback and cancellation during retry; earlier backup/chart/cache/review safety checks retained. Close-audit/cleanup suite:14 passed. Full logic:2377 passed,0 failed; one pre-existing Python/Unix chart retry check skipped. At normal and simulated125% scale in EN/FA:84 launch/role/selection/time-layout checks,30 progress/stop checks,82 table/name/note/hover checks passed per run. Actual wide layout screenshot inspected: report age under Today and the former time column blank. Installer version/payload/resources, package integrity, and remote download hashes verified before delivery. Windows folder/ACL behavior and broker execution require user-side validation; injected Linux tests do not reproduce the user's native denial.
