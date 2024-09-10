[]{#/movement_mode var (world).md}    
## movement_mode var (world)    
**See also:**    
:   [appearance_flags var (atom)](/atom/var/appearance_flags)    
:   [Enter proc (atom)](/atom/proc/Enter)    
:   [Exit proc (atom)](/atom/proc/Exit)    
:   [Cross proc (atom)](/atom/proc/Cross)    
:   [Uncross proc (atom)](/atom/proc/Uncross)    
:   [Pixel movement](/%7Bnotes%7D/pixel-movement)    
:   [Gliding](/%7Bnotes%7D/gliding)    
<!-- -->    
**Possible values:**    
:   `LEGACY_MOVEMENT_MODE`: Old BYOND behavior regarding pixel movement    
    and turf contents (see below)    
:   `TILE_MOVEMENT_MODE`: All atoms are locked to the tile grid    
:   `PIXEL_MOVEMENT_MODE`: All movable atoms can use pixel movement    
    unless otherwise specified (see below), but legacy behavior for turf    
    contents is ignored    
<!-- -->    
**Default value:**    
:   LEGACY_MOVEMENT_MODE    
Controls how movement works on the map.    
`TILE_MOVEMENT_MODE` allows you to easily discard any and all pixel    
movement, so if step_x or step_y coordinates or unexpected atom bounds    
were loaded from a savefile, for instance, they would be eliminated. If    
you use any other movement mode, you can give an atom the    
[TILE_MOVER](/atom/var/appearance_flags){.code} flag and it will behave    
as if it were in this mode, while other atoms are free to do their own    
thing.    
`LEGACY_MOVEMENT_MODE` exists to distinguish between old and new    
movement behavior. In older versions of BYOND before pixel movement,    
turfs took their contents into consideration by default in Enter() and    
Exit(). This doesn\'t really make sense for newer games, so in any other    
movement mode the turf behavior will ignore its contents. mob.Cross() is    
also affected, since it would return 0 by default in legacy mode when    
both mobs were dense; now by default it checks `mob.group`.  