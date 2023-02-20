##### Function : Calendaring and Scheduling
##### Schedule_GetFirstDetails - Returns the handle to the first detail object for the schedule.
---
```
#include <schedule.h>
STATUS LNPUBLIC Schedule_GetFirstDetails(

	HCNTNR  hCntnr,
	HSCHEDULE  hSchedObj,
	HCNTNROBJ *rethDetailObj,
	SCHED__DETAIL_LIST FAR * FAR *retpDetail);
```
**Description :**

Returns the handle to the first detail object for the schedule.

**Parameters :**
Input :
hCntnr  -  Handle of container to get details from.

hSchedObj  -  Handle to the current schedule.

Output :
(routine)  -  Return status from this call: 

NOERROR 

ERR_xxx - Other errors returned by this function and includes errors returned by lower level functions. Call OSLoadString to obtain a string to display to the user.


rethDetailObj  -  Points to the handle to the detail.

retpDetail  -  Points to the poiner to the detail.


**See Also :**
[HCNTNR](/reference/Data/HCNTNR)
[HCNTNROBJ](/reference/Data/HCNTNROBJ)
[HSCHEDULE](/reference/Data/HSCHEDULE)
[SCHED_DETAIL_DATA](/reference/Data/SCHED_DETAIL_DATA)
[SCHED_DETAIL_ENTRY](/reference/Data/SCHED_DETAIL_ENTRY)
[SCHED_DETAIL_LIST](/reference/Data/SCHED_DETAIL_LIST)
---