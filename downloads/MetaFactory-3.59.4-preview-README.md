# MetaFactory 3.59.4 preview

Approved minimal main-list polish: student names have a thin gray rounded outline following the existing row background; hover turns the name and border blue. The separate student-note action is now one simple pencil: gray when empty, blue when a note exists. Its click target and editor are unchanged.

In Account information, the title Overall DD is now Maximum DD, using the same previously verified whole-account relative balance drawdown value. Balance and Maximum DD labels use muted gray; monetary and percentage values are dark regular weight, without heavy bold. This is a label and presentation change only: no change to drawdown definition, financial calculations, stored data, import, sorting, broker processes or delivery behavior. Earlier 9pt server/copy fonts, green Live indicator and Send plane are retained.

Validation: compiled using Microsoft .NET Framework 4.5 reference assemblies. Existing account/report UI/model smoke checks run at normal and 125% scale. Real Windows/broker execution is not newly tested.

Validation outcome: existing UI/model checks passed 55 normal +55 at125% (0 failures). Generated normal and hover UI screenshots reviewed. Assembly/resource versions and embedded installer payload verified. Validation used synthetic Mono UI, not new real broker execution.
