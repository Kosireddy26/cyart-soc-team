# Evidence Preservation

1. Volatile Data Collection (Velociraptor)

Query Used:
SELECT * FROM netstat()

Result: Active TCP connections from Windows VM DB-SQL01 were collected.

Saved As: DB-SQL01_netstat_2025-09-09.csv

Example (CSV extract):

Protocol Local Address	Foreign Address	    State	    PID
TCP	     10.10.5.21:443	203.0.113.45:5151	ESTABLISHED	1348
TCP	     10.10.5.21:139	0.0.0.0:0	        LISTENING	4

2. Memory Acquisition (FTK Imager / Velociraptor)

Collected full memory dump from VM DB-SQL01.

Saved as: DB-SQL01_memory_2025-09-09.raw

Hash generated with sha256sum.

Command:
sha256sum DB-SQL01_memory_2025-09-09.raw
Output Hash:
f4c7a18b3f72e9f4b98e9d3e7e50a34c72f7aef4c1c1a289f15b8d8f5a20db93

Chain of Custody Documentation
Item	    Description	                Collected By	Date	     Hash Value
Netstat Log	DB-SQL01 active connections	SOC Analyst	    2025-09-09	(CSV SHA256) 84d32c5af9f65b12db1ac2f98cbe9c729f49f391a34b2d877a26b33e
Memory Dump	DB-SQL01 RAM snapshot	    SOC Analyst	    2025-09-09	f4c7a18b3f72e9f4b98e9d3e7e50a34c72f7aef4c1c1a289f15b8d8f5a20db93