# MetaFactory 3.57.0 preview — compact student actions

The per-student ellipsis/right-click menu now has exactly three top-level commands:
- Edit information: the existing account editor, titled clearly and made narrower, supports trader name, account number, server, investor password and the existing optional master/sign-in mode. Passwords start masked; existing encrypted storage and validation are retained.
- Copy: student name, account number, server, or account information together. This general information text excludes passwords.
- Close: chart review, live report, or both; choices reflect the row's currently observed open roles. Existing close/queue guards are retained. The main toolbar still supports group operations.

Each row's edit/copy/close command targets that student, even when other students are ticked or the focused grid row changes. A missing context target cannot fall back to another student's account.

Clicking a student's name continues to open their report. A compact Manage button on that page holds the less frequent commands: terminal opening/showing, chart review showing, refresh, folder assignment, copy-folder access, existing password copy, report-copy rebuild, force close and student/copy deletion. Existing deletion/rebuild confirmations and backup rules are retained. These management actions target the displayed student independently of ticks on the list. Password copy retains its clipboard timeout.

Empty copies can also open their information page, so folder/delete management remains accessible before an account is saved. The page displays no financial data for an empty copy. The report presentation refresh key includes the account binding/has-account state so removal or a changed account cannot leave an earlier rendered account view in place.

No native reporter, terminal launch transport or financial formula change is included. The prior automatic Telegram/Bale token connection flow is retained. Public artifacts contain no supplied bot tokens/private connection files.

Verification uses synthetic accounts on .NET/Mono with English/Persian UI checks at normal and125percent scaling, including editing/persistence, clipboard contents/secret exclusion, exact row targeting, close role availability, management access, empty copies and header bounds. Application tests and installer payload/version checks are recorded with the release. These checks do not establish new real broker/API executions on Windows.
