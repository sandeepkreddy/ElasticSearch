# ElasticSearch
* Elastic search is a opensource serch server based on apache lucene
* Written in java
* Designed to take data from any source , analyze it and search through it.
* Communication with elastic serever is done through http rest api
     e.g : curl -X <REST Verb> <Node> :<Port>/<index>/<Type>/<ID>
* Schema less json documents (like NoSql databases)
* Developed by elastic search BV which provides commercial solutions related to elastic search
* Near Real Time Search.

## Definitions

### CLUSTER
* A Cluster is a collection of nodes
* Consists of one or more nodes depending on the scale.
* Together all these nodes contain all data
* A cluster provides indexing and search capabilities cross all nodes.
* Identified by unique Name( Default to "elasticSearch")

## NODE
* A single sever that is part of a cluster.
* Stores searchable data
* stores all the data if there is only one node in the cluster , or stores part of the data if a cluster has multiple nodes
* Partipates in a cluster indexing and search capabilities
* Each node is identifies by a name (defaults to a random Marvel Character)
* A node joins a cluster named "elasticsearch" by default unless otherwise configured.

##Index
* A collection of documents (e.g : customer,account etc)
   * Each of the above example can be a type
* Corresponds to a database with in a relational database system , this analogy applies for most of the cases but not for all.
* Identified by a name which must be **lowercased**
* This name is used when indexing,updating,deleting documents with in an index.
* you can define as many indexes as you want with in a cluster.

##Document
* With in an index are types of documents
* Document is a basic unit of information that can be indexed 
* Consists of key value pairs , a value can be of various types such as string,date,object etc.
* 
* Represents a category/class of similar documents ,e.g : checkingaccount,savingsaccount, etc.
* Consists of a name and a mapping
* Simplified , you can think of type as a table in relational database.
* An index can have one or more types defined depending on their mapping.
* Stored under metadata field named _type because Lucene has no concept of document types
* Searching for a specified document types applies a filter on this field.

##Mapping
* Similar to schema in a relation databse , a mapping describes the fields that a document of a given type may have , this includes
  the data types for each feild , e.g. string,integer,date ....
* Also includes information on how the fields should be indexed and stored by lucene.
* If no mapping is specified mapping of a document is done dynamicall by infering the data that is supplied.
