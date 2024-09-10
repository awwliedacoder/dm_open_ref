[]{#/size var (vector).md}    
## size var (vector) {#size-var-vector byondver="516"}    
**See also:**    
:   [vector](/vector)    
:   [vars (vector)](/vector/var)    
The magnitude of this vector. Magnitude is the square root of the    
summed-up squares of all its components. For instance in 3D:    
size = x\*x + y\*y + z\*z    
`V.size` is the same as `sqrt(V.Dot(V))`.    
This value can be set at runtime, so setting `size = 1` will normalize    
the vector.    
If the size is already 0, as in the case of a degenerate vector like    
0,0, then changing this value will have no effect.  