# MetaFactory 3.68.2 preview

Show the measured desktop heap size in its settings dialog.

- Display Active current desktop size separately from Configured registry value. The active reading uses the existing read-only LaunchCapacityDiagnostics.CaptureResources observer-desktop metric (GetUserObjectInformation/UOI_HEAPSIZE) on the dialog's desktop thread.
- Show unavailable when that metric cannot be read. Never substitute the registry value, the recommendation or zero as an active measurement. Format displayed values with invariant Latin digits in both UI languages.
- Explain that the measurement belongs to this application's desktop. Other sessions/desktops can differ; a registry change may need a restart. A mismatch is not automatically labeled as proof of a pending reboot, and the reading is heap size, not free RAM or a terminal-count limit.
- Keep the existing20480KB recommended maximum, supported choices, backup/UAC/restart flow and oversized-write rejection unchanged. Opening this dialog performs no registry write and does not change Windows settings.

Scope: HeapDialog display only, plus version metadata/tests/docs. The Heap registry read/write/validation body is byte-equivalent to3.68.1. Import queue, parser/prompt, terminal launch/close, native verification/live/reporting, financial calculations, bots and storage unchanged.

Validation:74 focused UI/guard checks across100%/125%, Persian/English, a1366x768 test screen and fa-IR numeric culture. Synthetic active/registry values are intentionally different, unknown active never borrows the registry value, unknown registry does not hide a measured active value, oversized readings never enable unsupported choices, and20481/40960/65536 writes remain rejected by the pure validation function. Final Framework4.5 build, assembly/PE versions, embedded probes and exact installer payload verified. Windows live API reading was already present in diagnostics; real Windows reading on the user's computer is not measured from this Linux/Mono test environment. No OS setting was applied during testing.

Installer: MetaFactory-Setup-3.68.2-preview.exe
Full source, blank template and existing prompt: MetaFactory-3.68.2-preview-Full-Package.zip
