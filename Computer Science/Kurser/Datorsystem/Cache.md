#Kurs/Datorsystem 

# Cache-minne
***
Purpose of cache memory  
– to speed up accesses -> storing recently used  
data closer to the CPU.  
• Cache is smaller than main memory.  
• Access time is a fraction of main memory.  
• Cache is accessed by content  
– it is often called content addressable memory.  
• A single large cache memory -> it takes longer to  
search.

19  
• Content addressable cache memory is  
– subset of the bits of a  
main memory address -> field.  
– Many blocks of main memory map to a single block of  
cache  
– A tag field in the cache block distinguishes one  
cached memory block from another.  
– A valid bit indicates -> the cache block is being used.  
– An offset field points to the desired data in the block.


- Store items that have been used recently for faster access
- Based on the notion of [[Locality|locality]].
- Cashing can be done using [[Register|registers]], [[Primärminne|RAM]] or [[Hard disk]] etc.


CPU:n letar först i cache-minnet efter en instruktion, sedan i arbetsminnet.


Small amount of fast memory  
• Sits between normal main memory an CPU  
• May be located on CPU chip or module


The CPU initially looks in the Cache for the data it needs  
• If the data is there, it will retrieve it and process it  
• If the data is not there then the CPU accesses the system  
memory and then puts a copy of the new data in the cache  
before processing it.  
• Next time if the CPU needs to access the same data again it  
will just retrieve the data from the cache instead of going  
through the loading process again.


• EXAMPLE Consider a word-addressable main memory  
consisting of 4 blocks, and a cache with 2 blocks, where  
each block is 4 words.  
– First, we need to determine the address format for mapping.  
Each block is 4 words, so the offset field must contain 2 bits;  
there are 2 blocks in cache, so the block field must contain 1 bit;  
this leaves 1 bit for the tag (as a main memory address has 4 bits  
because there are a total of 2 4 =16 words).

• In set associative cache mapping, a memory  
reference is divided into three fields: tag, set,  
and offset.  
• As with direct-mapped cache, the offset field  
chooses the word within the cache block, and  
the tag field uniquely identifies the memory  
address.  
• The set field determines the set to which the  
memory block maps.

## [[Associative cache]]
## [[Direct mapped cache]]

## [[Cache replacement policy]]

## [[Cache coherence]]