# C++ Example Of An Efficient 3 Dimensional Heap Allocated Array
  This "3d array" is optimized by using two linear arrays (one for pointers, one for data).  Once set up, it is accessed using 3 dimensions.
  
### Why This Is Better
  The usual way of implementing a 3D *heap* allocated array seems to be by making D1xD2xD3 heap allocations, which can result in fragmented memory.
  
  The performance concious way of doing it would be to use a single dimensional array and simulate multi dimensions by calculating, on the fly, how to access the elements.  This method is not as nice to use.
  
  The method below allocates a linear data array, and sets up a linear pointer array to give 3 dimensional access to the data array:  The elements are accessed in the usual way (eg. pA[1][2][3]).  And since there are only two heap allocations, it should be fairly efficient in terms of CPU cache, etc.
