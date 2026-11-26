# MetaFactory 3.61.1 preview

- Restores red Delete student and copy… at the bottom of the main row menu. The action targets that exact row, retains the existing confirmation/recycle-bin workflow and refuses deletion of running copies.
- Marks repeated account numbers with Duplicate below the account number; hover lists matching students, copies and servers. Adds a Duplicates view to find these rows.
- Duplicate detection covers the complete roster before folder/platform filtering, uses account number only, normalizes Persian/Arabic digits and leading zeroes, and ignores missing/invalid/zero account numbers. Same name with different accounts is not a duplicate. No account is deleted automatically.
- Keeps 3.61.0 account/range PF/DD, All history, main folder column and folder actions.

Validation uses synthetic roster data on Mono/Linux, English/Persian and normal/125% layout checks; native Windows Recycle Bin behavior and broker execution not newly tested.

Installer: MetaFactory-Setup-3.61.1-preview.exe
Full package includes source and blank student Excel template, with no private bot connection files or real student credentials.
