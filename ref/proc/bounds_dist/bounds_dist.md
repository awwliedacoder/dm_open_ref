[]{#/proc/bounds_dist}
## bounds_dist proc
**See also:**
:   [bound_x var (movable atom)](#/atom/movable/var/bound_x)
:   [bound_y var (movable atom)](#/atom/movable/var/bound_y)
:   [bound_width var (movable atom)](#/atom/movable/var/bound_width)
:   [bound_height var (movable atom)](#/atom/movable/var/bound_height)
:   [step_x var (movable atom)](#/atom/movable/var/step_x)
:   [step_y var (movable atom)](#/atom/movable/var/step_y)
:   [bounds proc](#/proc/bounds)
:   [Pixel movement](#/%7Bnotes%7D/pixel-movement)
<!-- -->
**Format:**
:   bounds_dist(Ref, Target)
<!-- -->
**Returns:**
:   The distance, in pixels, between Ref\'s and Target\'s bounding
    boxes.
<!-- -->
**Args:**
:   Ref: A turf, obj, or mob.
:   Target: A turf, obj, or mob.
The value returned by bounds_dist() is the number of pixels that the two
objects would have to move closer together (if this is even possible, of
course) to be touching but not overlapping.
A return value of 12 for instance means the two objects have a gap of 12
pixels between them.
A return value of 0 means the two objects are not overlapping, but their
bounding boxes touch.
A return value of -2 means the two objects are overlapping by 2 pixels;
they would have to move 2 pixels apart to separate.