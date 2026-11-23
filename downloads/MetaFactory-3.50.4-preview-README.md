# MetaFactory 3.50.4 preview

Fixes MT5 live daily-report validation: the native exporter now supplies classified deal details required to reconcile today’s full-history events. Missing details previously left accounts pending even with a fresh heartbeat and complete history. Existing validation and financial calculations remain unchanged. MT4, appearance, queue and update/UAC behavior are unchanged.

Close MetaFactory and the running MT5 terminals, install, then reopen the same MT5 copies in Live mode. MT4 terminals may remain open. The changed MT5 expert may compile once on first use. Send a full System Check about two minutes after the last launch. This fixes a confirmed data-contract defect, not every possible startup delay or resource limit.

Validation: 2330 checks passed, zero failures; one existing Python chart-retry check skipped in Mono. Assembly/PE/resource versions, installer payload, embedded native source and source-scope audit verified. Actual Windows/MetaEditor/broker execution is not available here and needs confirmation on the user’s computer. Automatic UAC approval is not implemented by this release.
