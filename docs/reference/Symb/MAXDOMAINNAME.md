##### Symbolic Value : Limits
##### MAXDOMAINNAME - Maximum management domain name.
---
```
#include <names.h>
```
**Description :**

This length includes the terminating null so it may be used in data 
declarations.  However, in places where a size is specified that indicates the 
maximum number of characters in the name, then the symbol minus 1 should be 
used.

**See Also :**
[MailGetDomainName](/reference/Func/MailGetDomainName)
[MailGetMessageOriginatorDomain](/reference/Func/MailGetMessageOriginatorDomain)
---