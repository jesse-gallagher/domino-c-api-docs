##### Data Type : Item (Field) Information
##### ITEM_DEFINITION_TABLE_LOCK - Database Item Definition Table (Extended) locked Information.
---
```
#include <nsfdb.h>
```

**Definition :**
```
typedef struct {
   DWORD Items;
   void *pItemDefArray;
   char *ItemText[MAX_ITEMDEF_SEGMENTS];
   DWORD NumSegments;
   DWORD ItemNameSegLengths[MAX_ITEMDEF_SEGMENTS];
} ITEM_DEFINITION_TABLE_LOCK;
```

**Description :**

This structure is used with the ITEM_DEFINITION_TABLE_EXT and ITEM_DEFINITION_EXT structures that contain the Item Definition Table (Extended) information.  The information within this structure contains pointers to handles that are in the other structures, and some copies of other members.  The fields in this structure are:
<ul><br>
<br>
Items							A copy of the number of items in the table<br>
pItemDefArray						A pointer to ITEM_DEFINITION_EXT structures<br>
ItemText							A pointer to packed text segments<br>
NumSegments						A copy of the number of non-null segments of packed text.<br>
ItemNameSegLengths[MAX_ITEMDEF_SEGMENTS]	A copy of the length of each non-null text segment.<br>
  <br>
The user passes a pointer to this structure as input to the following NSF functions:<br>
NSFItemDefExtLock, NSFItemDefExtUnlock, NSFItemDefExtEntries, NSFItemDefExtGetEntry</ul>



**See Also :**
[ITEM_DEFINITION_EXT](/domino-c-api-docs/reference/Data/ITEM_DEFINITION_EXT)
[ITEM_DEFINITION_TABLE_EXT](/domino-c-api-docs/reference/Data/ITEM_DEFINITION_TABLE_EXT)
[NSFDbItemDefTableExt](/domino-c-api-docs/reference/Func/NSFDbItemDefTableExt)
[NSFItemDefExtEntries](/domino-c-api-docs/reference/Func/NSFItemDefExtEntries)
[NSFItemDefExtFree](/domino-c-api-docs/reference/Func/NSFItemDefExtFree)
[NSFItemDefExtGetEntry](/domino-c-api-docs/reference/Func/NSFItemDefExtGetEntry)
[NSFItemDefExtLock](/domino-c-api-docs/reference/Func/NSFItemDefExtLock)
[NSFItemDefExtUnlock](/domino-c-api-docs/reference/Func/NSFItemDefExtUnlock)
---
