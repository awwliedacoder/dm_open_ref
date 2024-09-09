[]{#/proc/step_away}
## step_away proc
**See also:**
:   [get_step_away proc](#/proc/get_step_away)
:   [walk_away proc](#/proc/walk_away)
:   [step_size var (movable atom)](#/atom/movable/var/step_size)
<!-- -->
**Format:**
:   step_away(Ref,Trg,Max=5,Speed=0)
<!-- -->
**Returns:**
:   1 on success; 0 otherwise.
<!-- -->
**Args:**
:   Ref: A mob or obj.
:   Trg: An object on the map.
:   Max: The maximum distance between Ref and Targ before movement
    halts.
:   Speed: Speed to move, in pixels. 0 uses Ref.step_size.
Move Ref on a path away from location Trg, taking obstacles into
account. If Ref is farther than Max steps from Trg, no action will be
taken.