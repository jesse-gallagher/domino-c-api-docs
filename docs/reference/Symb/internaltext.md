##### Symbolic Value : Resource Definition
##### internaltext - Assign an error code number to a text string.
---
```
#include <globerr.h>
```
**Description :**

Assigns the given error code to the given text string.  When language 
compiling, the macro actually amounts to nothing more than a comment.  When 
resource compiling a module (RC), the macro is used to map error code numbers 
to a corresponding text string.

Prior to Release 4.5, an alternative form was defined due to a compiler bug in 
MPW C.  The compiler generated an error when a macro evaluated to nothing and 
is followed by another #define.


/* "internaltext" designates STATUS codes used to indicate a condition
 passed between 2 subsystems, but NEVER displayed to a user. The text
 associated with "internaltext" is NOT EVEN STORED in the executables,
 and thus, never translated or shown to a user. */

#define internaltext(code,text)


**Sample Usage :**
```
#define ERR_QUEUE_NOT_EMPTY PKG_MISC+1
 internaltext(ERR_QUEUE_NOT_EMPTY, "Deleting a non-empty queue")
#define ERR_QUEUE_EMPTY   PKG_MISC+2
 internaltext(ERR_QUEUE_EMPTY,  "No more entries to dequeue")
```
**See Also :**
[errortext](/reference/Symb/errortext)
[helptext](/reference/Symb/helptext)
[debugtext](/reference/Symb/debugtext)
[stringtext](/reference/Symb/stringtext)
[apitext](/reference/Symb/apitext)
[blocktext](/reference/Symb/blocktext)
[semtext](/reference/Symb/semtext)
[donottranslatetext](/reference/Symb/donottranslatetext)
[limitedasciitext](/reference/Symb/limitedasciitext)
---