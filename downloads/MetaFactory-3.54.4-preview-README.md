# MetaFactory 3.54.4 preview

## Changes
- Launch dropdown now follows the approved minimal two-row layout: approximately 220 x 80 logical pixels, a numeric spinner, Live checkbox, and a small charcoal Run button. No repeated title, selected-count caption, explanatory paragraph, or oversized action button. Main window size stays unchanged.
- Every opening starts with one instance. Count 2 means one primary plus one ordinary review copy. Live/ordinary primary selection and all explicit-launch/cancel behavior are retained. Persian and Latin typed digits are supported; count stays within the existing 1..200 range.
- Selection fix: ticks are scoped to the current filtered account list. When switching search/status/platform/folder filters, picks hidden by the resulting filter are removed from both the badge and batch targets. Returning to All does not silently restore old picks. Scrolling retains ticks on offscreen rows in the same list. Folder tick shortcuts first display that folder and respect the active filters.
- Existing review-only / primary-only / both close commands and process ownership protections are preserved. Native live reporting, financial calculations, update policy, and broker runtime are unchanged.

## Install
Close MetaFactory, then run MetaFactory-Setup-3.54.4-preview.exe. Existing account/settings/note data and terminal copies use the same installer behavior.

## Validation
Built against Microsoft .NET Framework 4.5 reference assemblies. UI checks in English/Persian at normal and simulated 125% scale cover compact geometry, no resize, Persian digit entry/bounds, explicit confirmation, no cancel side effects, a reproduced hidden-third-selection case, exact batch target count, checkbox consistency, no restored hidden ticks, scrolling preservation, and close-by-type through harmless sleeper processes. Existing launch-stop/completion checks and installer version/payload/resource checks passed. The full logic suite passes 2,376 checks, 0 failures; one pre-existing Python/Unix chart retry check is skipped. Linux tests do not validate native Windows broker connectivity, update prompts, or graceful chart saving in MetaTrader.
