# MetaFactory 3.54.3 preview

## Changes
- Compact anchored Run dropdown replaces the separate launch dialog. About 296 x 204 logical pixels; no main-window resizing. It contains copies per student, the live-report option and an explicit Run button. Each opening defaults to one copy; changing the count or dismissing the menu launches nothing.
- Count 2 opens one primary plus one ordinary chart-review instance per selected student; higher counts add ordinary review instances. Existing running copies are reused. The prior ordinary primary mode remains available through the live-report checkbox.
- Close/Close open and the row close command offer review-only, primary-only, or both. Review-only keeps all primary live-report processes open. The existing selected list determines scope; Close open applies to all accounts. Primary-only stops live reporting for those primaries.
- Closing by type uses the exact classified list without re-expanding it to both types. Existing process ownership and graceful-close protections remain. Wait for launch preparation/queue to settle or stop the launch queue before closing by type.
- Menus have no effect until an explicit command; count is not saved. No new automatic launches. Closing the menu leaves selection unchanged; accepted actions retain existing selection clearing.

## Install
Close MetaFactory, then run MetaFactory-Setup-3.54.3-preview.exe. Existing accounts, settings, notes and broker terminal copies are preserved by the existing installer.

## Validation
Built against Microsoft .NET Framework 4.5 reference assemblies. 2,376 logic checks passed, 0 failed; one existing Python/Unix chart retry check skipped. Compact menu tests in English/Persian at normal and simulated 125% scale cover defaults, cancel/no side effects, explicit launch, no window resizing, one/selected/all scope, 30 primary plus 30 review classification, and exact closing via harmless sleeper processes. Existing launch completion/stop checks and embedded installer payload/version checks passed. Native report/EA/runtime files are unchanged. Native Windows broker connectivity, update prompts, and graceful chart-saving are not exercised by these Linux tests.
