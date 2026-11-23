# MetaFactory 3.50.5 preview

Corrects a 3.50.4 native MT5 export defect: detailed D deal rows are MTR extension rows, while the END count covers only J/T/O/B rows. Counting D incorrectly caused otherwise valid histories to fail completeness checks. The exporter now follows the existing reader/writer contract. Daily deal classifications from 3.50.4 remain available; no financial validation is relaxed.

MT4, calculations, original appearance, launch pacing and update/UAC behavior are unchanged. This fixes confirmed history rejection, not all terminal startup latency. Close MetaFactory and running MT5 copies before installing, then open the same MT5 accounts in Live mode. MT4 may remain open. First launch can compile the changed expert once. Send full System Check about two minutes after the last launch.

Validation details are in source/VERIFICATION-3.50.5.json. Actual MetaEditor compilation and live broker execution require Windows confirmation. Automatic UAC approval is not implemented.
