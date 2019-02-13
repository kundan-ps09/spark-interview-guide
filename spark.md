# Spark Interview Questions And Answers
So, here is the Spark Interview Questions list which contains all types of interview Questions asked in Spark interview.

**Q1. What is Apache Spark?**

**Ans.** Spark is: 
  
	- An open source big data framework. 
	- It has an expressive APIs to efficiently execute streaming as well as the batch. 
	- It provides faster and more general data processing platform engine. 
	- It is basically designed for fast computation. 
	- It was developed at UC Berkeley in 2009. 
	- It distributes data in file system across the cluster, and process that data in parallel. 
	- It covers a wide range of workloads like batch applications, iterative algorithms, 
	  interactive queries and streaming. 
	- It lets you write an application in Java, Python or Scala.
	- It was developed to overcome the limitations of MapReduce cluster computing paradigm. 
	- Spark keeps things in memory whereas map reduce keep shuffling things in and out of disk. 
	- It allows to cache data in memory. 
	- Spark is easier to develop as it knows how to operate on data. It supports SQL queries, 
	  streaming data as well as graph data processing. 
	- Spark doesn’t need Hadoop to run, it can run on its own using other storages like Cassandra, 
	  S3 from which spark can read and write. 
	- In terms of speed spark run programs up to 100x faster in memory or 10x faster on disk than Map Reduce.

**Q2. What is the need of Apache Spark?**

**Ans.**  Basically, we had so many general purpose cluster computing tools. 

For example:

	> Hadoop MapReduce, 
	> Apache Storm, 
	> Apache Impala, 
	> Apache Storm,
	> Apache Giraph and many more. 
But each one has some limitations in their functionality as well. Such as:

	1. Hadoop MapReduce can only allow for batch processing.
	2. If we talk about stream processing only Apache Storm / S4 can perform.
	3. Again for interactive processing, we need Apache Impala / Apache Tez.
	4. While we need to perform graph processing, we opt for Neo4j / Apache Giraph.

Therefore, No single engine can perform all the tasks together. hence there was a big demand for a powerful engine that can process the data in real-time (streaming) as well as in batch mode
Also, which can respond to sub-second and perform in-memory processing

