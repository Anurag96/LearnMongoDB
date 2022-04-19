# LearnMongoDB

What is data?
	The facts that can be stored or recorded.
What is database?
	The group of data that can be relate together.
	
OLAP & OLTP
OLTP : Online transactional processing : All those transaction takes place in the real-time/Dynamic data, provdies short term storage. Ex: OLTP => RDBMS => Oracle
OLAP : Offline analytical processing : Access all the processed/static or historical data, provdies long term storage. Ex: OLAP => DW => Netezza
NewSQL : Stores all application data, provdies long term storage. NoSQL => MongoDB

Evolution of Database
1.Flat file (IBM- Programmable sequencial file) 1960's
	Store and retrive information any time. 
Can't filter the data &cannot have a table structure there.
2.Hierarchey Database
	There is relation between each entity. As structure becomes bigger, it's difficult to get relation
	 between higher and lower chain structure.
3.DBMS 1970's 
	RDBMS : Entity based relationship model.
	Volume : It's designed to work with concentrated data, ie., limited data.
	Variety : It's designed to worked with structure/semi-strcutured data.
4.NoSQL database
	VVV - Volume,Variety, Velocity
	Volume : Huge storage of data,It's designed to work with distributed data.
	Variety : It's designed to worked with unstructure data.
	Velocity : NoSQL provides velocity becuase of it's flexibility with volume and variety.
	It was introduced to overcome drawback with SQL
	It has no schema or table structure
	It has distributed data.
	It support Replication of data
	It also support horizantal scaling of data ie., Sharding
	It also open source.
	NoSQL stores value in form of either 
		1.key-value pairs, 2. wide-column, 3. graph & 4. Documents.
	MongoDB is used to store JSON Documents. 
	Google : Bog Table & Amazon : Amazon DynamoDB => Initial NoSQL database
	
How to decide which database to use?
ACID ? BASE ? CAP ?

Properties :
RDBMS works on ACID properties:
ACID : Atomicity, Consistency,Isolation & Durability
	Atomicity : Database will commit if all the transcaction are successful, if any of them fails, then roll-back the commit.
	Consistency : Both parties involved in transaction must see same changes at the end of the transaction.
	Isolation : When two transaction is taking place,each transaction should be individual in their own.
	Durability : All the changes must be permanent, they should be volatile in nature.

NoSQL works on BASE properties:
BASE: Basically Available, Soft State & Eventually consistent
	Basically Available : Database is up & running, but won't be able to support all operations. 
		Ex: when server is down, transaction might not be possibl;e but one can see their status.
	Soft State : Able to move from one state to another state, It doesn't has to be write-consistent or all mutally consistent all the time.
	Eventually consistent : Same changes appeares eventually over a peroid of time.
		Ex: When one upload 300 pic on facebook, eventually it appears to all friends.

CAP Theorm : According to CAP theorm, no way any database in the world can display these 3 properties at same time,
	Consistency, Availabity, Partition Tolerance (Horizontal data scaling => 1TB + 1TB)
Ex:	
	MongoDb supports Consistency, Partition Tolerance
	RDBMS supports Availabity, Consistency
	Cassendra supports Availabity, Partition Tolerance
	
MongoDB Database
	It supports Consistency, Partition Tolerance
	It is also highly scablable
	It's highly Available,but not completely Available(Basically availability) 
	
	