##### Function : Character Manipulation
##### NLS_isalnum - Tests if a character is an uppercase or lowercase alphabetic or is a numeric digit.
---
```
#include <nls.h>
NLS_STATUS LNPUBLIC NLS_isalnum(

	const BYTE far *pCharacter,
	NLS_PINFO  pInfo);
```
**Description :**

This function tests if a character is an uppercase or lowercase alphabetic or 
is a numeric digit.

**Parameters :**
Input :
pCharacter  -  Pointer to the character to be tested.

pInfo  -  A pointer to an NLS_INFO struct, which contains all of the tables and attributes of the current character set. The NLS_INFO struct should have been initialized by a previous call to OSGetLMBCSCLS().

Output :
(routine)  -  NLS_SUCCESS - The specified character is an uppercase or lowercase alphabetic or is a numeric digit.
NLS_PROPNOTFOUND - The specified character is NOT an uppercase or lowercase alphabetic and is NOT a numeric digit.
NLS_INVALIDTABLE - pInfo->PropertyTable is NULL;



**See Also :**
[NLS_INFO](/domino-c-api-docs/reference/Data/NLS_INFO)
[NLS_isalpha](/domino-c-api-docs/reference/Func/NLS_isalpha)
[NLS_isarith](/domino-c-api-docs/reference/Func/NLS_isarith)
[NLS_iscntrl](/domino-c-api-docs/reference/Func/NLS_iscntrl)
[NLS_isdigit](/domino-c-api-docs/reference/Func/NLS_isdigit)
[NLS_isleadbyte](/domino-c-api-docs/reference/Func/NLS_isleadbyte)
[NLS_islower](/domino-c-api-docs/reference/Func/NLS_islower)
[NLS_ispunct](/domino-c-api-docs/reference/Func/NLS_ispunct)
[NLS_isspace](/domino-c-api-docs/reference/Func/NLS_isspace)
[NLS_isupper](/domino-c-api-docs/reference/Func/NLS_isupper)
[NLS_PINFO](/domino-c-api-docs/reference/Data/NLS_PINFO)
[OSGetLMBCSCLS](/domino-c-api-docs/reference/Func/OSGetLMBCSCLS)
---
