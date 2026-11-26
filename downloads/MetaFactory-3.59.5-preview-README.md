# MetaFactory 3.59.5 preview

Approved compact selection badge: checked icon + selected count + All [visible total], with the existing select-all link behavior and full accessible selected-count description. Batch targets, checkbox state and selection-clearing semantics are unchanged.

Account-information labels Balance and Maximum DD now use the same 9pt regular font as server text. Label width is measured with the actual drawing device context, extra glyph space, and no label ellipsis, fixing the Windows Ba... / Ma... rendering seen in the supplied screenshot. Titles remain muted gray and values dark. Financial values and formulas unchanged.

Existing UI/model checks passed 55 normal +55 at125%, zero failures. Real runtime selection/account-label screenshots inspected at both scales. Microsoft .NET Framework4.5 reference build, assembly/resource version and embedded installer payload verified. Synthetic Mono rendering does not constitute actual Windows/broker execution validation.
