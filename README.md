# CVE-2022-47529
RSA NetWitness Platform EDR Agent / Incorrect Access Control - Code Execution

During a security audit of the EDR agent I discovered a novel vector to tamper with the service with only standard user rights by targeting an insecure Win32 memory event object. Hijacking the service config can also be done if running the exploit as admin.

CVE-2022-47529 allows local users to stop the Endpoint Windows agent from sending the events to SIEM or make the agent run user-supplied commands.

Insecure Win32 memory objects in Endpoint Windows Agents in the NetWitness Platform through 12.x allow local
and admin Windows user accounts to modify the endpoint agent service configuration:
to either disable it completely or run user-supplied code or commands, thereby bypassing tamper-protection features via ACL modification.

Interestingly, the agent was uploaded to virustotal on 2022-01-05 17:24:32 UTC months before finding and report.

SHA-256 770005f9b2333bf713ec533ef1efd2b65083a5cfb9f8cbb805ccb2eba423cc3d
LANDeskService.exe

[Network Access]
Local


[References]
https://community.netwitness.com/t5/netwitness-platform-security/nw-2023-04-netwitness-platform-security-advisory-cve-2022-47529/ta-p/696935

