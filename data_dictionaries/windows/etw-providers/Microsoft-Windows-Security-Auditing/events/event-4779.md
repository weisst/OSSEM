# Event ID 4779: A session was disconnected from a Window Station
###### Version: 0

## Description
This event is generated when a user disconnects from an existing Terminal Services session, or when a user switches away from an existing desktop using Fast User Switching.

## Data Dictionary
|Standard Name|Field Name|Type|Description|Sample Value|
|---|---|---|---|---|
|user_name|AccountName|UnicodeString|the name of the account for which the session was disconnected.|`ladmin`|
|user_domain|AccountDomain|UnicodeString|subject's domain or computer name|`CONTOSO`|
|user_logon_id|LogonID|HexInt64|hexadecimal value that can help you correlate this event with recent events that might contain the same Logon ID|`0x1e01f6`|
|session_name|SessionName|UnicodeString|the name of disconnected session|`RDP-Tcp#6`|
|src_host_name|ClientName|UnicodeString|machine name from which the session was disconnected. Has "Unknown"value for console session.|`WIN81`|
|src_ip_addr|ClientAddress|UnicodeString|IP address of the computer from which the session was disconnected.|`10.0.0.100`|

## References
* [MS Source](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/master/windows/security/threat-protection/auditing/event-4779.md)
* [MS Security Auditing Category - Account Logon](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/advanced-security-audit-policy-settings#account-logon)
* [MS Security Auditing Category - Logon/Logoff](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/advanced-security-audit-policy-settings#logonlogoff)
* [MS Security Auditing Sub-category - Audit Other Logon/Logoff Events](https://github.com/MicrosoftDocs/windows-itpro-docs/tree/master/windows/security/threat-protection/auditing/audit-other-logon/logoff-events.md)

## Tags
* etw_level_Informational
* etw_task_task_0
* Account Logon
* Logon/Logoff
* Audit Other Logon/Logoff Events