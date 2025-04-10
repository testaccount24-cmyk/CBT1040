# CBT1040
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE1040 is from Frank Clarke, Oldsmar FL, and consists        *   FILE1040
//*           primarily of REXX EXECs and MACROs designed to        *   FILE1040
//*           operate on PL/I source elements and compiler          *   FILE1040
//*           listings.                                             *   FILE1040
//*                                                                 *   FILE1040
//*           Additional routines may be found in FILE433 in the    *   FILE1040
//*           CBT collection which serves as an adjunct to the      *   FILE1040
//*           code found here.                                      *   FILE1040
//*                                                                 *   FILE1040
//*           email:  Frank Clarke <rexxhead@yahoo.com>             *   FILE1040
//*                                                                 *   FILE1040
//*               'FCLARKE.PLIMACS.EXEC' - Directory                *   FILE1040
//*                                                                 *   FILE1040
//*                 Usage or                                        *   FILE1040
//*       Member    Caller      Description                         *   FILE1040
//*       ========  =========   =================================   *   FILE1040
//*                                                                 *   FILE1040
//*       @@README  text        About the material in this          *   FILE1040
//*                             library                             *   FILE1040
//*                                                                 *   FILE1040
//*       @FIL1040  text        Inventory                           *   FILE1040
//*                                                                 *   FILE1040
//*       @PLIEXMP  PLI         The pro-forma pattern for a new     *   FILE1040
//*                             PLI paragraph                       *   FILE1040
//*                                                                 *   FILE1040
//*       ADDXREF   exec        Add ISPF statistics to a            *   FILE1040
//*                             compiler listing                    *   FILE1040
//*                                                                 *   FILE1040
//*       ALLPLIB   macro       Queue all PLIBs from the listing    *   FILE1040
//*                             dataset                             *   FILE1040
//*                                                                 *   FILE1040
//*       CALLEDBY  macro       CALLs and their targets             *   FILE1040
//*                                                                 *   FILE1040
//*       COMBINE   exec        Combine 2 or more datasets with     *   FILE1040
//*                             incompat DCBs                       *   FILE1040
//*                                                                 *   FILE1040
//*       COMPARM   exec        Maintain parameters for COMPILE     *   FILE1040
//*                                                                 *   FILE1040
//*       COMPDT    exec        Reports the compile-date for        *   FILE1040
//*                             LOAD modules                        *   FILE1040
//*                                                                 *   FILE1040
//*       COMPILE   exec        Background compile of foreground    *   FILE1040
//*                             source                              *   FILE1040
//*                                                                 *   FILE1040
//*       COMPSTAT  macro       For listings, sets member stats     *   FILE1040
//*                                                                 *   FILE1040
//*       DENUM     macro       Denumber source in listing          *   FILE1040
//*                             dataset                             *   FILE1040
//*                                                                 *   FILE1040
//*       ELEMENTS  macro       For listings, display Attribute     *   FILE1040
//*                             list                                *   FILE1040
//*                                                                 *   FILE1040
//*       ELEMLEN   exec        Calc storage needed for a           *   FILE1040
//*                             variable                            *   FILE1040
//*                                                                 *   FILE1040
//*       ENTCOMM   macro       Adjust END statements for           *   FILE1040
//*                             Enterprise compiler                 *   FILE1040
//*                                                                 *   FILE1040
//*       IOSTMT    macro       Show all I/O statements             *   FILE1040
//*                                                                 *   FILE1040
//*       LCOMM     macro       Insert line comment                 *   FILE1040
//*                                                                 *   FILE1040
//*       ONEPERLN  macro       Splits PL/I source lines            *   FILE1040
//*                                                                 *   FILE1040
//*       PARSEDCL  macro       Annotate structure DCL with         *   FILE1040
//*                             column info                         *   FILE1040
//*                                                                 *   FILE1040
//*       PGFS      macro       Show all paragraph names            *   FILE1040
//*                                                                 *   FILE1040
//*       PLIFLOW   macro       Shows CALLs, GOTOs, and targets     *   FILE1040
//*                                                                 *   FILE1040
//*       PLILBLS   macro       Like PLIFLOW; show labels and       *   FILE1040
//*                             referents                           *   FILE1040
//*                                                                 *   FILE1040
//*       PLIMSGE   macro       Puts error msgs in-line on          *   FILE1040
//*                             listings (Enterprise)               *   FILE1040
//*                                                                 *   FILE1040
//*       PLIMSGO   macro       Puts error msgs in-line on          *   FILE1040
//*                             listings (Optimizer)                *   FILE1040
//*                                                                 *   FILE1040
//*       PLIMSGS   macro       Driver for PLIMSGE and PLIMSGO      *   FILE1040
//*                                                                 *   FILE1040
//*       PLINIT    macro       Adds initialization to PL/I DCL     *   FILE1040
//*                                                                 *   FILE1040
//*       PLIPARA   macro       Insert new empty paragraph          *   FILE1040
//*                                                                 *   FILE1040
//*       PLIPOS    macro       Similar to PARSEDCL                 *   FILE1040
//*                                                                 *   FILE1040
//*       PLISKIP   macro       Replace carr-ctl with               *   FILE1040
//*                             preprocessor cmds                   *   FILE1040
//*                                                                 *   FILE1040
//*       PLIXREF   macro       Adds stmt# refs to a listing        *   FILE1040
//*                             (driver)                            *   FILE1040
//*                                                                 *   FILE1040
//*       PLIXREFE  macro       ~~ for Enterprise                   *   FILE1040
//*                                                                 *   FILE1040
//*       PLIXREFO  macro       ~~ for Optimizer                    *   FILE1040
//*                                                                 *   FILE1040
//*       QIO       macro       Find and count all files by type    *   FILE1040
//*                                                                 *   FILE1040
//*       QJAM      macro       Check that all stmt#s are present   *   FILE1040
//*                                                                 *   FILE1040
//*       QSQL      macro       Analyze all the SQL statements      *   FILE1040
//*                                                                 *   FILE1040
//*       SEGMENT   macro       Label start and end of compiler     *   FILE1040
//*                             sections                            *   FILE1040
//*                                                                 *   FILE1040
//*       SHORTPG   macro       Excise spurious blank line from     *   FILE1040
//*                             listing                             *   FILE1040
//*                                                                 *   FILE1040
//*       SLICKIO   macro       (Source) align all file DCLs        *   FILE1040
//*                                                                 *   FILE1040
//*       SPLITDO   macro       Split if...do                       *   FILE1040
//*                                                                 *   FILE1040
//*       TRIMPLI   macro       Excise billions of SQL junk from    *   FILE1040
//*                             listing                             *   FILE1040
//*                                                                 *   FILE1040
//*       WHATINC   macro       Return on stack all %INC object     *   FILE1040
//*                             names                               *   FILE1040
//*                                                                 *   FILE1040
```
