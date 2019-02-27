# malloc
this version realize multiple threads and lock
it realizes malloc function


In this assignment, I implemented 4 memory allocation functions, ff_malloc( ), bf_malloc( ),ff_free( ), bf_free( ). 


To sum up, data_segment_size is the heap_size and we use a global variable to record it through each iteration allocation. Data_segment_free_space is total free space size through each iteration. Fragmentation is data_segment_free_space/data_segment_size. Execution time is not constant, may be it is due to server speed. The execution time is different between bf and ff, because first fit will find the address at the first time, while for  best fit, it will compare the allocated space with each other and choose the best one to  record. Moreover, because large_range_rand_allocs needs to allocate more chunk’s size than small_range_rand_allocs, it will take more time in my according my design. Because I do not use freeList to quickly find free place in equal_size, so it will take long time to execute. To get result, I change num_items to 100 to get result. Last but no least, ff may waste more space than bf, for it will return at the first time when finding enough space and separate, during separate process, it will have some fragmentation, because even though some unused space will save, this space may be to small for the further given size to use. 


Due to my long execution time, I will add freeList in my future design. In this design, it will record all free address, malloc in the freeList, merge the freeList when next and curr are next to each other. Due to limited time, I do not realize this function.
