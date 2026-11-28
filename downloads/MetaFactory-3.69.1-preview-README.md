# MetaFactory 3.69.1 preview

Fix the native MT5 prelaunch update-cache backup collision.

The supplied application log conclusively showed: IOException A preserved update cache already exists; nothing overwritten. The update-pause guard aborted before PID creation for one managed copy. No authentication result or native crash was established by that failure.

- If a current liveupdate directory and a preserved backup already coexist, leave the previous backup in place and rename the current cache to a fresh unique backup. Do not overwrite, merge or delete updater contents. A versioned, per-copy-key-bound owned marker records which backup is the current restore target.
- A flushed temporary owned marker acts as a move journal and is atomically published after the directory rename. Recover a single unambiguous interrupted transition; preserve and report unknown, foreign, linked or ambiguous states rather than guessing.
- Restore the current tracked cache, retaining the older backup. Keep the owned record until restoration succeeds so an interrupted restoration remains recoverable. Repeated hold/restart/restore cycles do not duplicate the current updater data. Moves stay within the same cache folder; this does not copy terminal histories or create another full runtime.
- Retain legacy version1 marker support. Reject path traversal and foreign-copy ownership. Validate backup type/link state before removing an owned marker. Missing uniquely tracked data retains its record and returns an explicit error.
- Keep the existing user setting enabled and keep the same per-copy cache scope, UAC/consent behavior, executable bytes, network policy and ownership guards. This does not globally enable updates, modify other copies' cache state or delete account files. No OS/client changes were performed from the development environment.

Scope: Mt5UpdatePolicy cache hold/restore transaction only, version metadata, focused tests and the obsolete collision-failure regression updated to successful preservation/restoration. Import single-pass20s behavior, parser/prompt, normal startup configuration, native authentication/report/live calculations, heap settings, bots and storage unchanged.

Validation uses a faithful local filesystem reproduction with synthetic updater bytes, including a pre-existing backup directory or file, restart/reacquisition, latest-cache restoration, repeated-cycle size behavior, interrupted move recovery, ambiguous state preservation, foreign marker, cross-copy pointer, traversal and missing-backup guards. Actual Windows filesystem locks/antivirus/vendor updater and the affected user's terminal must still be retried. This fixes the proven prelaunch collision; it does not certify broker login or rule out another independent launch failure.

Installer: MetaFactory-Setup-3.69.1-preview.exe
Full source, blank template and existing prompt: MetaFactory-3.69.1-preview-Full-Package.zip

Validation:2945 automated checks passed, including19new cache-collision/recovery checks,2427main,46Python and the existing fast-import/parser/workspace/phase/UI/replacement/live regressions. One existing chart retry check skipped for its Python environment requirement. Final Framework4.5 build, PE/assembly versions, embedded probes and exact installer payload verified.
