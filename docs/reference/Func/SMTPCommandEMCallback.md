##### Function : Extension Manager
##### SMTPCommandEMCallback - Extension Manager callback for EM_SMTPCOMMAND
---
```
#include <extmgr.h>
STATUS LNPUBLIC SMTPCommandEMCallback(

	DWORD  SessionID,
	char *Command,
	DWORD  MaxCommandLength,
	char *SMTPReply,
	DWORD  SMTPReplyLength);
```
**Description :**

EM_SMTPCOMMAND is called whenever a SMTP command has been received by the SMTP 
task.
	
The Extension Manager EM_BEFORE notification type for the EM_SMTPCOMMAND event 
occurs whenever a SMTP command has been received by the SMTP listener task but 
prior to the parsing of the command. 
	
Domino allocates a buffer that can be used by callback routines for the 
EM_BEFORE notification to modify the command and thus change internal Domino 
processing.  NOERROR return status indicates to skip parsing and execution of 
command.  The default reply when STATUS is NOERROR is "250 OK".  Return STATUS 
values other than ERR_EM_CONTINUE and NOERROR from the EM_BEFORE notification 
results in the command being rejected.  A default error message will be 
generated by the Domino SMTP server, which can be modified by the callback 
routine for the EM_AFTER notification.  When you reject the command for the 
SMTPConnect event with an error code,  the SMTP client will not be 
disconnected.   STATUS of ERR_EM_CONTINUE will continue normal Domino 
processing.
	
SMTP response to the command entered can be modified during the callback 
routine of EM_AFTER notification.  Care must be taken not to change the reply 
code from success to failure or vice-versa as this will cause the sender-SMTP 
and receiver-SMTP servers to be out of synch.  Domino supplies a buffer that 
can be used by the callback routine to change the SMTP response.

**Parameters :**
Input :
SessionID  -  Unique session identifier for the current session.

Command  -  NULL terminated string containing SMTP command and arguments received.

MaxCommandLength  -   Size of buffer allocated to modify Command.   EM_BEFORE event: Command can be modified in buffer provided

SMTPReplyLength  -  Size of buffer allocated to modify SMTPReply.

Output :
(routine)  -  Return status from the call 
EM_BEFORE event: NOERROR skips command parsing/execution.  Value other than ERR_EM_CONTINUE indicates that the callback routine has rejected the command.  
EM_AFTER event: Value other than ERR_EM_CONTINUE is ignored.


SMTPReply  -  SMTP response that will be returned to the connecting host.  EM_BEFORE event: NULL.  EM_AFTER event: NULL terminated string containing the SMTP response that will be returned to the connecting host.  Callback routine can modify the string.


**See Also :**
[EM_xxx](/reference/Symb/EM_xxx)
---