[]{#/Splice proc (list).md}    
## Splice proc (list) {#splice-proc-list byondver="514"}    
**See also:**    
:   [Copy proc (list)](/list/proc/Copy)    
:   [Cut proc (list)](/list/proc/Cut)    
:   [Insert proc (list)](/list/proc/Insert)    
:   [splicetext proc](/proc/splicetext)    
<!-- -->    
**Format:**    
:   list.Splice(Start=1,End=0,Item1,Item2\...)    
<!-- -->    
**Args:**    
:   Start: The list index where the splice will begin.    
:   End: The index immediately following the last item to be cut from    
    the list. 0 is the end of the list.    
:   Item1, Item2\...: Items to be inserted.    
Cuts out items from a list, and inserts new items in their place. This    
is basically equivalent to calling `list.Cut(Start,End)` and then    
calling `list.Insert(Start,Item1,Item2...)`, but faster.    
### Example:    
var/list/L = list(\"apple\",\"banana\",\"orange\",\"pear\") // cuts    
\"banana\" and \"orange\" and inserts four new items    
L.Splice(2,4,\"firetruck\",\"camel\",\"joystick\",\"balloon\") // prints    
apple, firetruck, camel, joystick, balloon, pear for(var/item in L) usr    
\<\< item    
As with `Insert()`, any items that are lists will insert their contents    
instead of themselves.    
The `Start` and `End` index values can be negative, which count    
backwards from the end of the list. If the index values are out of    
range, there will be no error; they will simply be clamped to the    
beginning or end of the list. If `End` comes before `Start`, the two    
values are swapped.    
Note: This proc doesn\'t work with many special lists such as `contents`    
or `overlays`.  