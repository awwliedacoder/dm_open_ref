[]{#/step_x var (movable atom).md}    
## step_x var (movable atom) {#step_x-var-movable-atom byondver="490"}    
**See also:**    
:   [step_y var (movable atom)](/atom/movable/var/step_y)    
:   [step_size var (movable atom)](/atom/movable/var/step_size)    
:   [bound_x var (movable atom)](/atom/movable/var/bound_x)    
:   [Move proc (movable atom)](/atom/movable/proc/Move)    
:   [locs list var (movable atom)](/atom/movable/var/locs)    
:   [Pixel movement](/%7Bnotes%7D/pixel-movement)    
<!-- -->    
**Default value:**    
:   0    
This var defines the position of the atom (in pixels) relative to its    
tile, on the x axis. A step_x of 5 means the atom actually is shown 5    
pixels east of the tile\'s western edge.    
The atom\'s actual bounding box may not begin at step_x, but can be set    
even further in via bound_x.    
Example: A 16×16 smiley face centered in a 32×32 icon should have the    
following bounds:    
-   bound_x = 8    
-   bound_y = 8    
-   bound_width = 16    
-   bound_height = 16    
For the smiley to appear at the left edge of the tile it is standing on,    
it would need a step_x value of -8. A step_x value of 8 takes it all the    
way to the rightmost edge of the tile. Anything outside of the range -8    
to 8 will have the atom straddling multiple turfs.  