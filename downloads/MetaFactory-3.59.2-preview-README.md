# MetaFactory 3.59.2 preview

Today again displays signed profit/loss, total trades (today closed plus currently open), and an Open marker only when positions are open. Live/report age stays on the second line. Overall DD stays only in Account information. Ordinary reports retain realized PnL; live reports use the existing net including floating PnL. Unverified total/amount remains unknown; pending-live floating results retain the syncing label. Main sorting and report result spacing are unchanged.

Includes a text-formatted Excel template and a fixed Persian AI extraction prompt. Name duplicates with distinct account numbers remain independent; existing import duplicate detection is account-number-only and unchanged. New import workflow improvements are proposals, not implemented in this release.

Validation: Microsoft .NET Framework 4.5 reference build; 55 existing account/report UI/model checks at normal scale and 55 at 125%, all passed. Actual UI screenshot reviewed. New workbook read by the actual importer with a synthetic fixture: long text account, password preservation, same-name distinct accounts, duplicate-number skip verified. Assembly/resource versions and embedded installer payload verified. Financial/native/report parsing logic unchanged; no new real broker execution validation.
