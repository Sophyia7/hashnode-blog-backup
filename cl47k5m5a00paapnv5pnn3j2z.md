## Horizontal vs. Vertical Scaling – How to Scale a Database

## Data Scalability

Data scalability is the ability of a database to manipulate changing demands by adding and removing data. It is a means by which a database grows at the same pace as the software. The database can expand or contrast the capacity of the system's resources to support the application's frequent changing usage.  

**There are two ways a database can be scaled:**
- Horizontal scaling ( Scale-up)
- Vertical scaling(Scale-out)

### The Horizontal Scaling
This scaling approach adds more database nodes to handle the increased workload. It decreases the load on the server rather than expanding the individual servers. When more capacity is needed, the user can add more servers to the cluster. Another name for this scaling method is **Scaling out**. 



![scaling out.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1654698852830/_z2erldoi.jpg align="left")

**Advantages of Horizontal Scaling:**
- It is easy to upgrade,
- It is simple to implement and costs less. 
- It offers flexible, scalable tools. 
- It has limitless scaling with unlimited addition of server instances.
- Upgrading a horizontally scaled database is easy - add a node to the server. 

**Disadvantages of Horizontal Scaling:**
- The bugs in the code will become more complex to debug and understand.
- The licensing fee is expensive as you will have more nodes that are more licensed.
- The cost of the data center will increase significantly because of the increased space, cooling, and power.

**When to use:**
- If you are dealing with more than a thousand users, it is best to use this scaling system because when the servers receive multiple user requests, it will scale well.
- It will not crash because there are multiple servers.


### The Vertical Scaling
The vertical scaling approach increases the capacity of a single machine by increasing the resources in the same logical server. This involves adding resources like memory, storage, and processing power to existing software, enhancing its performance. This is the traditional method of scaling a database. Another name for this approach is called, **Scale-up**.


![02vertical-scaling-software-scalability.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1654698928844/4MLBEGr4K.jpg align="left")


**Advantages of Vertical Scaling:**
- The cost of the data center for the space, cooling, and power will be less.
- It is a cost-efficient software. 
- It is easy to use and implement - the administrative can easily manage and maintain the software.
- The resources for this approach are flexible.

**Disadvantages of Vertical Scaling:**
- The cost may be low, but you will need to pay for a license each time you scale up.
- The hardware costs more because of high-end servers.
- There is a limit to the upgrade.  
- You are restricted to a single database vendor, and migration is challenging, or you may need to start over. 

**When to use:**
- The vertical scaling approach is for you if you need a system with unique data consistency.
- If you don't want to worry about balancing the server's workload, vertical scaling is the best for you. 

## The differences between vertical and horizontal

| Vertical | Horizontal |
|:----------|:--------|
|The license is cost less| The license is cost more|
|This method increases the power of the server with the individual server| This method increases the power of the server with the existing server 
| This data is present on one single node, and it is scaled through a multicore | This is based on partitioning each node that contains a single part of data.

## Which is suitable for your app?
When choosing how to scale your database, you must consider what's at stake when you scale up and out. We will take a look at some scenarios so you can choose which scaling system is best for your app:

- **Load balancing**: The vertical scaling system is best for balancing load because you have a single server (vertical scaling), and there is no need to balance your load, but the horizontal scaling system requires you to balance the workload evenly.

- **Point of failure**: The horizontal scaling system has more than one server, so when one server crashes, the next one picks up the slack, and there is no single point of failure which makes it resilient, but in the vertical scaling system, there is only one server, so once the server crashes, everything goes offline.  

- **Speed**:  In terms of speed, the vertical scaling system is faster because due to running on one server, the vertical scaling system has an Interprocess communication, i.e., the server communicates within itself and is fast. The horizontal scaling system has network calls between two or more servers; this could also be called Remote Procedure Calls(RPC). The RPC is slow, though.

- ** Data consistency**: When dealing with servers, you must ensure that the data stored in them is consistent when end users send a request. The vertical scaling system is data consistent because all information is on a single server, but the horizontal scaling system is scaled out with multiple servers, so data consistency is a huge issue. 

- **Hardware limitation**: The horizontal scaling system scales well because the amount of servers you throw at a problem is linear to the number of users in the database or server, and the vertical scaling system has a limitation because everything runs on a single server.

When choosing a system to scale your database, make sure to make a pros and cons list of the information in this article; it will help you come to a conclusion of which to use. 

## Conclusion

In conclusion, a cloud computing model's scalability is the ability to quickly and instantly increase or decrease an IT capacity. 
Knowing the two types of scalabilities is crucial as this plays a massive role in your database or server management. 

Quick recap...
- A server's role is to enhance its capacity to handle the increased workload, called Vertical scaling.
- A system's job is to add new nodes to manage the distributed workload, termed Horizontal scaling. 
- The horizontal scaling system scales well as the number of users increases. 
- The vertical scaling system is faster due to its ability to inter-process communication. 

Thanks for reading! 

### Keep in touch:
You can contact me via email and/or Twitter:

Email - iroegbusophia3@gmail.com

Twitter - sophiairoegbu_



























