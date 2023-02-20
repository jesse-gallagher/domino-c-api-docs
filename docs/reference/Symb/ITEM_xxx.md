##### Symbolic Value : Field
##### ITEM_xxx - Flags attached to an item in a note.
---
```
#include <nsfnote.h>
```
**Description :**

These flags define the characteristics of an item (field) in a note.  The flags 
may be bitwise or'ed together for combined functionality.

**Sample Usage :**
```
    if (error = NSFItemAppend ( hNote, 
                                ITEM_SUMMARY | ITEM_READWRITERS | ITEM_NAMES,
                                DISCUSS_ITEM_AUTHOR,  /* "Author" */
                                strlen(DISCUSS_ITEM_AUTHOR),
                                TYPE_TEXT,
                                szAuthor,
                                strlen(szAuthor)))
    {
        printf ("Error: unable to append Author field.\n");
    }
```
**See Also :**
[ITEM_xxx [NAMES]](/reference/Symb/ITEM_xxx [NAMES])
[ITEM_xxx [READERS]](/reference/Symb/ITEM_xxx [READERS])
[ITEM_xxx [READWRITERS]](/reference/Symb/ITEM_xxx [READWRITERS])
[NSFItemAppend](/reference/Func/NSFItemAppend)
[TYPE_xxx](/reference/Symb/TYPE_xxx)
---