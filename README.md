# dbmsImplnProject

  This script generates data according to the Wisconsin benchmark specification, as described in “The Wisconsin Benchmark: Past, Present, and Future” by David J. DeWitt. In order to follow the benchmark specification as closely as possible, I followed the code laid out in that document and simply ported it to golang.
  
We chose postgreSQL beacuse of the exposure to it in the previous courses and the ease of working with a stable system which executes faster and also since it's a relational database system. 

We read the Wisconsin benchamrk paper and learnt how databases can be efficiently benchmarked and how different database system flaws were corrected over the years using it as a standard for measuring their performance. 

The following are the two main objectives for the design of Wisconsin benchmark as quoted in the paper and those are the two objectives we are about to realize having taken the first step of generating data for benchmark.
"The benchmark was designed with two objectives in mind. First, the queries in the benchmark should test the performance of the major components of a relational database system. Second, the semantics and statistics of the underlying relations should be well understood so that it is easy to add new queries and to their behavior."
The benchmark was popular and it set the standard for measuring performanace of various relational database systems at that time and stayed strong with various vendors competing with each other by showing off their commericial database systems.




 

