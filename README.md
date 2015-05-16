# cache-map-reduce
Simple Map-Reduce interface implementation for Caché ObjectScript

Map-Reduce is implemented via global-based pipe ("global" here is the name
Caché persistent, hierarchical array.

There are several samples of Map-Reduce application, all of them are counting 
words in the set of input files ("War and Peace" in Russian by Leo Tolstoy):

* MR.Sample.WordCountMapReduce - count number of words for each file separately;
* MR.Sample.WordCountMapReduceSum - count words in files and calculate their total sum;
* MR.Sample.WordCountMapReduceWorkers - count words concurrently, using `%SYSTEM.WorkMgr` for parallel execution.

The next step - is to use `%Net.RemoteConnection` for remote execution and coordination.
