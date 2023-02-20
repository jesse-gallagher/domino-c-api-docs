##### Function : Message Queues
##### MQCreate - Create a message queue.
---
```
#include <mq.h>
STATUS LNPUBLIC MQCreate(

	const char far *QueueName,
	WORD  Quota,
	DWORD  Options);
```
**Description :**

Create a message queue with the specified name. Message queues provide Domino 
and Notes applications with inter-process communication capabilities.  A 
subsequent call to MQOpen is required to use this message queue.

**Parameters :**
Input :
QueueName  -  A pointer to the name to be assigned to the message queue.

Quota  -  Maximum number of messages that the queue may contain. Set this to zero for the default maximum.  The default maximum number of messages that the queue may contain is MAXWORD.

Options  -  Reserved. Must be 0.

Output :
(routine)  -  Return status from this call -- indicates either success or what the error is. The return codes include:

NOERROR
ERR_DUPLICATE_MQ - A message queue with the specified name already exists.
ERR_xxx - Errors returned by lower level functions.  There are so many possible causes, that It is best to use the code in a call to OSLoadString and display/log the error for the user.




**See Also :**
[MQClose](/reference/Func/MQClose)
[MQGet](/reference/Func/MQGet)
[MQHANDLE](/reference/Data/MQHANDLE)
[MQIsQuitPending](/reference/Func/MQIsQuitPending)
[MQOpen](/reference/Func/MQOpen)
[MQPut](/reference/Func/MQPut)
[MQPutQuitMsg](/reference/Func/MQPutQuitMsg)
[MQScan](/reference/Func/MQScan)
[MQSCAN_CALLBACK](/reference/Data/MQSCAN_CALLBACK)
---