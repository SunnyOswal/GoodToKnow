+ **Availability**  
defines the proportion of time that the system is functional and working. It will be affected by system errors, infrastructure problems, malicious attacks, and system load. It is usually **measured as a percentage of uptime**. Cloud applications typically provide users with a service level agreement (SLA), which means that applications must be designed and implemented in a way that maximizes availability.

  + **Health Endpoint Monitoring**  
  Implement functional checks in an application that external tools can access through exposed endpoints at regular intervals.
  + **Queue-Based Load Leveling**  
  Use a queue that acts as a buffer between a task and a service that it invokes in order to smooth intermittent heavy loads.
  + **Throttling**  
  Control the consumption of resources used by an instance of an application, an individual tenant, or an entire service.

+ **Management and Monitoring**  
Cloud applications run in a remote datacenter where you do not have full control of the infrastructure or, in some cases, the operating system. This can make management and monitoring more difficult than an on-premises deployment. Applications must expose runtime information that administrators and operators can use to manage and monitor the system, as well as supporting changing business requirements and customization without requiring the application to be stopped or redeployed.

  + **Ambassador**  
  Create helper services that send network requests on behalf of a consumer service or application.
  + **Anti-Corruption Layer**  
  Implement a façade or adapter layer between a modern application and a legacy system.
  + **External Configuration Store**  
  Move configuration information out of the application deployment package to a centralized location.
  + **Gateway Aggregation**  
  Use a gateway to aggregate multiple individual requests into a single request.
  + **Gateway Offloading**  
  Offload shared or specialized service functionality to a gateway proxy.
  + **Gateway Routing**  
  Route requests to multiple services using a single endpoint.
  + **Health Endpoint Monitoring**  
  Implement functional checks in an application that external tools can access through exposed endpoints at regular intervals.
  + **Sidecar**  
  Deploy components of an application into a separate process or container to provide isolation and encapsulation.
  + **Strangler**  
  Incrementally migrate a legacy system by gradually replacing specific pieces of functionality with new applications and services.

+ **Performance**  
is an indication of the responsiveness of a system to execute any action within a given time interval, while scalability is ability of a system either to handle increases in load without impact on performance or for the available resources to be readily increased. Cloud applications typically encounter variable workloads and peaks in activity. Predicting these, especially in a multi-tenant scenario, is almost impossible. Instead, applications should be able to scale out within limits to meet peaks in demand, and scale in when demand decreases. Scalability concerns not just compute instances, but other elements such as data storage, messaging infrastructure, and more.

  + Cache-Aside  
  Load data on demand into a cache from a data store
  + **CQRS**  
  Segregate operations that read data from operations that update data by using separate interfaces.
  + **Event Sourcing**  
  Use an append-only store to record the full series of events that describe actions taken on data in a domain.
  + **Index Table**  
  Create indexes over the fields in data stores that are frequently referenced by queries.
  + **Materialized View**  
  Generate prepopulated views over the data in one or more data stores when the data isn't ideally formatted for required query operations.
  + **Priority Queue**  
  Prioritize requests sent to services so that requests with a higher priority are received and processed more quickly than those with a lower priority.
  + **Queue-Based Load Leveling**  
  Use a queue that acts as a buffer between a task and a service that it invokes in order to smooth intermittent heavy loads.
  + **Sharding**  
  Divide a data store into a set of horizontal partitions or shards.
  + **Static Content Hosting**  
  Deploy static content to a cloud-based storage service that can deliver them directly to the client.
  + **Throttling**  
  Control the consumption of resources used by an instance of an application, an individual tenant, or an entire service.

+ **Resiliency**  
is the ability of a system to gracefully handle and recover from failures. The nature of cloud hosting, where applications are often multi-tenant, use shared platform services, compete for resources and bandwidth, communicate over the Internet, and run on commodity hardware means there is an increased likelihood that both transient and more permanent faults will arise. Detecting failures, and recovering quickly and efficiently, is necessary to maintain resiliency.

  + **Bulkhead**  
  Isolate elements of an application into pools so that if one fails, the others will continue to function.
  + **Circuit Breaker**  
  Handle faults that might take a variable amount of time to fix when connecting to a remote service or resource.
  + **Compensating Transaction**  
  Undo the work performed by a series of steps, which together define an eventually consistent operation.
  + **Health Endpoint Monitoring**  
  Implement functional checks in an application that external tools can access through exposed endpoints at regular intervals.
  + **Leader Election**  
  Coordinate the actions performed by a collection of collaborating task instances in a distributed application by electing one instance as the leader that assumes responsibility for managing the other instances.
  + **Queue-Based Load Leveling**  
  Use a queue that acts as a buffer between a task and a service that it invokes in order to smooth intermittent heavy loads.
  + **Retry**  
  Enable an application to handle anticipated, temporary failures when it tries to connect to a service or network resource by transparently retrying an operation that's previously failed.
  + **Scheduler Agent Supervisor**  
  Coordinate a set of actions across a distributed set of services and other remote resources.
