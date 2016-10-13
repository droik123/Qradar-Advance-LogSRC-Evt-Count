# Qradar-Advance-LogSRC-Evt-Count
This is an Advance ariel database query which pulls the information of the count of event received from a log source. 


select LOGSOURCENAME(logsourceid), COUNT() from events WHERE ((((((LOGSOURCENAME(logsourceid) <> 'Custom Rule Engine-8 :: [Hostnamehere]' AND LOGSOURCENAME(logsourceid) <> 'System Notification-2 :: [Hostnamehere]') AND LOGSOURCENAME(logsourceid) <> 'Health Metrics-2 :: [Hostnamehere]') AND LOGSOURCENAME(logsourceid) <> 'SIM Audit-2 :: [Hostnamehere]') AND LOGSOURCENAME(logsourceid) <> 'Asset Profiler-2 :: [Hostnamehere]') AND LOGSOURCENAME(logsourceid) <> 'SIM Generic Log DSM-7 :: [Hostnamehere]') AND LOGSOURCENAME(logsourceid) <> 'Search Results-2 :: [Hostnamehere]') AND LOGSOURCENAME(logsourceid) <> 'Anomaly Detection Engine-2 :: [Hostnamehere]' GROUP BY LOGSOURCENAME(logsourceid)
