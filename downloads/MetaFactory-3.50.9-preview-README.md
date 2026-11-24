# MetaFactory 3.50.9 preview: launch progress and Stop

Adds a bottom progress strip matching report progress for manual launch batches. Shows processed/total, percent, failures, remaining and current copy/preparation/waiting stage. Completion means the launch queue has been processed, NOT that every terminal window/login/livefinancialreport is ready. Individual dashboard readiness remains independently validated.

Stop launching clears remaining queued starts and stops pacing. It does not close/kill alreadyrunning terminals. A current async launcher may finish (and its one terminal may appear); the strip shows stopping until it settles. Missing-copy file preparation observes cooperative cancellation. Late completion cannot launch the next queued copy. A stopped partial run stays partial; a new batch resets it. Individual queue removal is counted as cancelled. New runs wait for an in-flight stopped operation to settle.

2374logicchecks passed0failed, one existingPythonchartretry skip. ActualMainForm with injected launcher and real testhelper:15UIchecks each in English/Persian verifiedstop event, queueclearing, no secondlaunch/no kill, latecompletionpartial50percent, nextbatchreset and failureprogress. App/installerPE/resources/payload/sourceauditverified. LinuxMono/Xvfb testing is not actualWindowsDPI/MetaTrader/broker verification; Persianoffscreenfontshaping is not Windowsvisualproof.

The3.50.8 noautomaticMT5updateoption remains unchanged/defaultON. Financial math, native collector1.05,MT4,bridge and launchpacingunchanged. This release does not newly proveUACsuppression or improvehardwarecapacity.

Close MetaFactory/install/reopen; healthy terminals may remainopen. Select2or3closedcopies and Run. The new bar appears at the bottom. Click Stop while copies remainqueued; alreadyrunningcopies stayopen and atmostthecurrentinflightstartmayfinish. Then try a new smallbatchaftersettling. No extraWatch/Synctoolneeded. SendfullSystemcheckiflaunch/updateproblemsremain.
