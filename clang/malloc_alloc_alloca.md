# alloc
alloc() is not a standard C library function. Some older compilers and libraries contain an <alloc.h> library which provides some memory allocation functions, but this is not standard. The Microsoft Visual C++ runtime includes an Alloc() function which is somewhat similar to malloc(), but this is also not part of the C standard. 
 
# malloc
malloc() allocates memory on the process heap. Memory allocated using malloc() will remain on the heap until it is freed using free(). 

# alloca
alloca() allocates memory within the current function's stack frame. Memory allocated using alloca() will be removed from the stack when the current function returns. alloca() is limited to small allocations. 

# difference
Situations where alloca() is appropriate are rare. In almost all situations, you should use malloc()to allocate memory. 
