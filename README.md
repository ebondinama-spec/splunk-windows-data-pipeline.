# splunk-windows-data-pipeline.
This project involved setting up a complete Splunk data pipeline to ingest Windows Event Logs and then performing detailed Root Cause Analysis (RCA) to resolve three distinct infrastructure-level failures. This is the most complex and valuable part of my portfolio.
Failure Point,Symptom,Technical Solution Implemented
Network Blockage,UF could not reach the Indexer port.,Created a Windows Firewall Inbound Rule to allow TCP traffic on port 9997.
Service Permissions,UF service lacked access to system logs.,Changed the SplunkForwarder service's Log On account to the Local Administrator to grant system-level read access.
Indexer Listening,Indexer received data but dropped it silently.,Created the Indexer's inputs.conf file in C:\Program Files\Splunk\etc\system\local\ and added the stanza: [splunktcp://9997]  stanza].
