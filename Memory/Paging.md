# Paging
Paging is a solution for [[Contiguous Memory Allocation#External Fragmentation | external fragmentation]] in [[Contiguous Memory Allocation | contiguous memory allocation]]. Blocks of the same, fixed size (called pages) are created as a block in [[Logical Address Space | logical address space]]. Frames are referred to as a block in [[Physical Address Space | physical address space]]. One page is allocated to one frame; thus, there is no contiguous requirement. This does cause [[Contiguous Memory Allocation#Internal Fragmentation | internal fragmentation]].
## Address Translation Scheme
A logical address is represented as a tuple <page number, offset>. The page number is an index to the page table and the offset is combined with the base address to define the physical memory address.
## Page Table
A page table is kept in main memory and is made up of two registers: 
1. Page-Table Base Register: points to page table.
2. Page-Table Length Register: indicates size of page table.
### Translation Look-Aside Buffer
This is high-speed associative memory used to store recently used page data for expedited lookup.