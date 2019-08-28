# Spark Interview Questions And Answers
So, here is the Spark Interview Questions list which contains all types of interview Questions asked in Spark interview.

**Q1. What is Apache Spark?**

**Ans.** Apache Spark is a lightning-fast unified analytics engine for big data and machine learning. 

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
	
	

**Spark vs Hadoop**

| Criteria | Hadoop MapReduce | Apache Spark |
| --- | --- | --- |
| Memory | Does not leverage  the memory of the  hadoop cluster to maximum. | Let's save data on memory with the use of RDD's. |
| Disk usage | MapReduce is disk oriented. | Spark caches data in-memory and ensures low latency. |
| Processing | Only batch processing is supported | Supports real-time processing through spark streaming.|
| Installation |Is bound to hadoop | Is not bound to Hadoop |

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
	
**Q8.**Various ways to create contexts in spark ?**

**Ans.** below are the verious way to create context

	a. Sparkconext
	b. Sqlcontext
	c. Sparksession
	d. Sqlcontext.sparkcontext
	
**set up the spark configuration and create contexts**

	val sparkConf = new SparkConf().setAppName("SparkSessionExample").setMaster("local")
	
**to SparkContext to access other context like SQLContext**

	val sc = new SparkContext(sparkConf).set("spark.some.config.option", "some-value")
        val sqlContext = new SQLContext(sc)
	
**Whereas in Spark 2.0 the same effects can be achieved through SparkSession, without expliciting creating SparkConf, SparkContext or SQLContext, as they’re encapsulated within the SparkSession. 


	val warehouseLocation = "file:${system:user.dir}/spark-warehouse"
	val spark = SparkSession
   	.builder()
   	.appName("SparkSessionsExample")
   	.config("spark.sql.warehouse.dir", warehouseLocation)
   	.enableHiveSupport()
   	.getOrCreate()
	
**Q9. What is RDD?**

RDDs (Resilient Distributed Datasets) are basic abstraction in Apache Spark that represent the data coming into the system in object format. RDDs are used for in-memory computations on large clusters, in a fault tolerant manner. RDDs are read-only portioned, collection of records, that are:


	-Resilient because RDDs are immutable(can’t bemodified once created) and fault tolerant
	 (If a node holding the partition fails the other node takes the data). 
	-Distributed because it is distributed across cluster.
	-Dataset because it holds data.
	
RDDs are automatically distributed across the network by means of Partitions. 
	
	-RDDs are divided into smaller chunks called Partitions, and when you execute some action,
	 a task is launched per partition. 
	-These partitions of an RDD is distributed across all the nodes in the network.
	
**Actions/Transformations:**
There are two types of operations that you can perform on an RDD- Transformations and Actions.

	Transformation:
        -Applies some function on a RDD and creates a new RDD, it does not modify the RDD that you apply 
	 the function on. (Remember that RDDs are resilient/immutable).
    	-Also, the new RDD keeps a pointer to it’s parent RDD.
	
 ![rdd_transformation](rdd_transformation.png)

When you call a transformation, Spark does not execute it immediately, instead it creates a lineage. A lineage keeps track of what all transformations has to be applied on that RDD, including from where it has to read the data. For example, consider the below example

![rdd_lineage](rdd_lineage.png)

	val rddTextFile = sparkSession.sparkContext.textFile("src/main/resources/bank-names.txt", 2)
	val rddContainNumber = rddTextFile.filter(line => line.contains("Number")) //transformation
  	println(rddTextFile.toDebugString)
  	println(rddContainNumber.toDebugString)
  	print(rddContainNumber.count())

* sparkSession.sparkContext.textFile() and rddTextFile.filter() do not get executed immediately.
* It will only get executed once you call an Action on the RDD - here rddContainNumber.count().
* An Action is used to either save result to some location or to display it.
* You can also print the RDD lineage information by using the command filtered.toDebugString(filtered is the RDD here).
	
**Caching**
You can cache an RDD in memory by calling rdd.cache(). When you cache an RDD, it’s Partitions are loaded into memory of the nodes that hold it.

	rddContainNumber.cache()
   	println(rddContainNumber.toDebugString)

![rdd_cache](rdd_cache.png)

Caching can improve the performance of your application to a great extent. In the previous section you saw that when an action is performed on a RDD, it executes it’s entire lineage. Now imagine you are going to perform an action multiple times on the same RDD which has a long lineage, this will cause an increase in execution time. Caching stores the computed result of the RDD in the memory thereby eliminating the need to recompute it every time. You can think of caching as if it is breaking the lineage, but it does remember the lineage so that it can be recomputed in case of a node failure.

**Persistence**
caching can be used to avoid recomputation of RDD lineage by saving its contents in memory. If there is not enough memory in the cluster, you can tell spark to use disk also for saving the RDD by using the method persist().
 
 	rddContainNumber.persist(StorageLevel.MEMORY_AND_DISK)
	println(rddContainNumber.toDebugString)
	
In fact Caching is a type of persistence with StorageLevel -MEMORY_ONLY. If you use MEMORY_ONLY as the Storage Level and if there is not enough memory in your cluster to hold the entire RDD, then some partitions of the RDD cannot be stored in memory and will have to be recomputed every time it is needed. If you don’t want this to happen, you can use the StorageLevel - MEMORY_AND_DISK in which if an RDD does not fit in memory, the partitions that do not fit are saved to disk.

![rdd_persistence](rdd_persistence.png)

In the above example, the RDD has 3 partitions and there are 2 nodes in the cluster. Also, memory available in the cluster can hold only 2 out of 3 partitions of the RDD. Here, partitions 1 and 2 can be saved in memory where as partition 3 will be saved to disk.
Another StorageLevel are :
 
 	DISK_ONLY: stores all the partitions on the disk.
	MEMORY_ONLY_SER: serialized before saving to Memory and store the RDDs as serialized java objects.
	MEMORY_AND_DISK_SER: rialized before saving to Memory and disk, and store the RDDs as serialized java objects.


**Q10.Why RDD is immutable ?**

Following are the reasons:

	– Immutable data is always safe to share across multiple processes as well as multiple threads.
	– Since RDD is immutable we can recreate the RDD any time. (From lineage graph).
	– If the computation is time-consuming, in that we can cache the RDD which result in performance improvement.




**Q9.Difference between map and flatmap?**

**Ans. **
