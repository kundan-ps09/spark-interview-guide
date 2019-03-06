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

	- Hadoop MapReduce
	- Apache Storm
	- Apache Impala
	- Apache Storm
	- Apache Giraph and many more. 
But each one has some limitations in their functionality as well. Such as:

	1. Hadoop MapReduce can only allow for batch processing.
	2. If we talk about stream processing only Apache Storm / S4 can perform.
	3. Again for interactive processing, we need Apache Impala / Apache Tez.
	4. While we need to perform graph processing, we opt for Neo4j / Apache Giraph.

Therefore, No single engine can perform all the tasks together. hence there was a big demand for a powerful engine that can process the data in real-time (streaming) as well as in batch mode
Also, which can respond to sub-second and perform in-memory processing

**Q3. What are the components of Spark Ecosystem?**

**Ans.** Apache spark consists of following components:

	1.Spark Core
	2.Spark SQL
	3.Spark Streaming
	4.MLlib
	5.GraphX

**Spark Core:** Spark Core contains the basic functionality of Spark, including components for task scheduling, memory management, fault recovery, interacting with storage systems, and more. Spark Core is also home to the API that defines resilient distributed datasets (RDDs), which are Spark’s main programming abstraction.It also provides many APIs for building and manipulating these RDDS.

**Spark SQL:** Spark SQL provides an interface to work with structured data.It allows querying in SQL as well as Apache Hivevariant of SQL(HQL).It supports many sources.

**Spark Streaming:** It is spark component that enables processing of live streams of data.

**MLlib:** Spark comes with common machine learning package called MLlib

**GraphX:** GraphX is a library for manipulating graphs (e.g., a social network’s friend graph)and performing graph-parallel computations.

**Q4. what is the basic data structure of Apache Spark Core?**

**Ans.** Spark Core is the fundamental unit of the whole Spark project. It provides all sort of functionalities like

	- Task dispatching
	- Scheduling
	- Input-output operations etc.
	
Spark makes use of Special data structure known as **RDD (Resilient Distributed Dataset)**. It is the home for API that defines and manipulate the RDDs. 

All the basic functionality of Apache Spark Like 

	- In-memory computation 
	- Fault tolerance
	- Memory management
	- Monitoring
	- Task scheduling 
	
is provided by Spark Core. Apart from this Spark also provides the basic connectivity with the data sources. For example, HBase, Amazon S3, HDFS etc.

**Q5.What are the benefits of Apache Spark over Apache Hadoop?**

**Ans.** Apache Spark is lightening fast cluster computing tool. It is up to 100 times faster than Hadoop MapReduce due to its very fast in-memory data analytics processing power.

Apache Spark surpasses Hadoop in many cases such as

	1. Processing the data in memory which is not possible in Hadoop.
	2. Processing the data that is in batch, iterative, interactive & streaming i.e. Real Time mode. 
	   Whereas Hadoop processes only in batch mode.
	3. Spark is faster because it reduces the number of disk read-write operations.
	   Whereas in Hadoop MapReduce intermediate output which is output of Map() is always written 
	   on local hard disk.
	4. Apache Spark is easy to program as it has hundreds of high-level operators 
	   with RDD (Resilient Distributed Dataset).
	5. Apache Spark code is compact due compared to Hadoop MapReduce. 
	   Use of Scala makes it very short, reduces programming efforts. 
	   Also, Spark provides rich APIs in various languages such as Java, Scala, Python, and R.
	6. Spark & Hadoop are both highly fault-tolerant.
	7. Spark application running in Hadoop clusters is up to 10 times faster on disk than Hadoop MapReduce.
	
**Q6. What are the different methods to run Spark over Apache Hadoop?**

**Ans.**  Instead of MapReduce we can use spark on top of Hadoop ecosyste

	- Spark with HDFS
	        you can read and write data in HDFS
	- Spark with Hive
		you can read and analyse and write back to the hive
**Q7. What is SparkContext in Apache Spark?**

**Ans.** A SparkContext is a client of Spark’s execution environment and it acts as the master of the Spark application. SparkContext sets up internal services and establishes a connection to a Spark execution environment. You can create RDDs, accumulators and broadcast variables, access Spark services and run jobs (until SparkContext stops) after the creation of SparkContext. Only one SparkContext may be active per JVM. You must stop() the active SparkContext before creating a new one.

The SparkContext allows the Spark driver application to access the cluster through a resource manager. The resource manager can be YARN, or Spark’s Cluster Manager.

**Few functionalities which SparkContext offers are:**

	1. We can get the current status of a Spark application like configuration, app name.
	2. We can set Configuration like master URL, default logging level.
	3. One can create Distributed Entities like RDDs.
