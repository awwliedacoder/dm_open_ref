[]{#/fps var (client).md}    
## fps var (client) {#fps-var-client byondver="511"}    
**See also:**    
:   [fps var (world)](/world/var/fps)    
:   [tick_lag var (client)](/client/var/tick_lag)    
:   [Pixel movement](/%7Bnotes%7D/pixel-movement)    
<!-- -->    
**Default value:**    
:   0 (uses world.fps value)    
This is a client version of world.fps, so that the client can run at a    
faster speed for animations. For example, setting client.fps to 40 while    
world.fps is the default 10 will mean that all animations and glides are    
smoothed out and displayed at 40 FPS, even though the server still runs    
at 10 FPS. The result is a nicer-looking game with no additional impact    
on the server.    
When this value is 0, the client and server tick at the same rate.  