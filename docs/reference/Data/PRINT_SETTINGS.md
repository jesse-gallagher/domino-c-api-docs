##### Data Type : Rich Text
##### PRINT_SETTINGS - Print Settings
---
```
#include <editods.h>
```
**Description :**

Print settings passed to editor export procedures.

Flags    Flags for print settings:  
	PS_Initialized  Print settings have been initialized
 PS_HeaderFooterOnFirst  Header and footer are printed on the first page
 PS_CropMarks  Crop marks will be printed
 PS_ChangeBin  Different paper bins will be used for the first page and all 
subsequent pages
	PS_HeaderFooterRTL  Paper source should be set for 1st & Other Pg.
	PS_ReleaseRightMargin  Release the right margin when printing (to print 
into gutter)
StartingPageNum Page number of first page
TopMargin Height in "twips" (1/1440 inch) between top of page and main body
BottomMargin Height in twips between bottom of page and main body
ExtraLeftMargin Additional left margin space in twips (beyond what's already 
specified in the document)
ExtraRightMargin Additional right margin space in twips (beyond what's already 
specified in the document)
HeaderMargin Height in twips between top of page and header
FooterMargin Height in twips between bottom of page and footer
PageWidth If non-zero, override the printer's page width with this dimension 
(in twips)
PageHeight If non-zero, override the printer's page height with this dimension 
(in twips)
BinFirstPage Index of paper bin to use for the first page
BinOtherPage Index of paper bin to use for all other pages
PageOrientation New in Notes/Domino 6.  0 = Undefined, 1 = Portrait, 2 = 
Landscape. See PSPO_xxx
wSpare   Spare word 
spare[2]   Spare dwords

**See Also :**
[EDITEXPORTDATA](/reference/Data/EDITEXPORTDATA)
[PRINTNEW_SETTINGS](/reference/Data/PRINTNEW_SETTINGS)
[PSPO_xxx](/reference/Symb/PSPO_xxx)
[PS_xxx](/reference/Symb/PS_xxx)
---