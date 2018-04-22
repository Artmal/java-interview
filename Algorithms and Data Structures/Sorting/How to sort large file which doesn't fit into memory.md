## How to sort a large file which doesn't fit into the RAM?
1. Chunk it to sub-arrays which fits into the memory.
2. Sort them in-place(quicksort).
3. Write result to temporary file/files.
4. Merge them.
