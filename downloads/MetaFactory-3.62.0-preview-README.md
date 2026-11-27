# MetaFactory 3.62.0 preview — storage retention

Automatic, while MetaFactory is open: after startup, then every 2 hours. Interrupted or larger batches retry after about 2 minutes. Sweeps yield to launch/preparation/repair/report work; they never stop a terminal.

- Native daily logs: expire over 7 days or reduce eligible older logs against a 50 MiB per-copy budget. Today, yesterday, files modified within 24h and locked files remain protected. This is not a hard cap on actively growing logs.
- Known abandoned live .part files: expire after 2 days without writes. Current snapshots/history are retained.
- Managed private-profile archives: retain the latest 2; extra named archives older than 7 days expire only when their contents are also old. Current profiles, personal chart files outside these obsolete private archives and account journals are not targeted.
- Review terminals are reused and their chart data is retained. Daily log/temp retention also covers known review copies.

Tools > Clean up unneeded files shows eligible categories and bytes in a scrolling preview. Old complete repair backups, abandoned staging folders and inactive binding output are manual opt-in only, unchecked by default. Old repair backups can be found after student removal; latest two and recent repair backups remain protected. Manual removals go to Recycle Bin, which must be emptied to recover actual disk space. Automatic expired-file cleanup deletes obsolete eligible files directly.

Linked roots/ancestors/subtrees and unknown filenames are excluded. Eligibility/process/binding state is checked again after the manual preview. Active terminal paths inside full backup/staging candidates are excluded. Required account data, passwords, current charts, price/trade history, current live bindings and report calculation sources are preserved.

Storage controls reduce redundant-file growth; necessary account history, retained backups and active logs can still grow. Existing app-log rotation and bounded report diagnostics remain in place.

Validation: synthetic filesystem cleanup, byte accounting, age/quota/retention tests, cancellation/late-write/in-use/symlink checks, EN/FA normal/125% layout and existing application regressions. Native Windows recycle-bin/locking and real broker behavior not newly exercised in this Linux environment.

Launch/close/native report source is retained from3.61.1; this release does not claim a fix for the separately reported39-concurrent-terminal issue. Bot redesign remains paused.

Installer: MetaFactory-Setup-3.62.0-preview.exe
Package includes source and a blank student Excel template. No private bot connection files or real student credentials.
