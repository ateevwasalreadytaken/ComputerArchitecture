# Computer Architecture
The theme of this project is cache design and how a caching processor generates and services address references.

This project will simulate a CPU cache (unified instruction/data) and integrate the cache into behavioral simulator. As the processor simulator executes an assembly-language program, it will access instructions and data. These accesses will be serviced by the cache, which will transfer data to/from memory as needed.


The cache function will simulate a cache with the following characteristics:

1) WRITE POLICY: write-back, allocate-on-write

2) ASSOCIATIVITY: varies according to the blocksPerSet parameter. Associativity ranges from 1 (direct-mapped) to the number of blocks in the cache (fully associative).

3) SIZE: the total number of words in the cache is blockSizeInWords * numberOfSets * blocksPerSet

4) BLOCK SIZE: varies according to the blockSizeInWords parameter. All transfers between the cache and memory take place in units of a single block.

5) PLACEMENT/REPLACEMENT POLICY: when looking for a block within a set to replace, the best block to replace is an invalid (empty) block. If there is none of these, replace the least-recently used block.
