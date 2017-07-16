# Frequently Asked Questions

##### What is a Blox scheduler?
Blox schedulers are responsible for making the decision of “what” to run and “when” to run a container or set of containers based on a customers specification of tasks and services. The scheduling decision may be based on: task or service health, event response, schedule, or other custom business logic. The Blox scheduler is enabled to take advantage of the Amazon EC2 Container Service (Amazon ECS) task placement options, such as: availability spread, binpacking, attribute-based placement, etc....  

##### What is a daemon scheduler?
A daemon scheduler runs one-task-per node on set of nodes. As new nodes join the cluster, the daemon scheduler identifies the new node and will automatically start a task on the node. The daemon scheduler also monitors the daemons running on every node and can restart the task as required. Common use cases for this scheduler include running logging or monitoring agents.

##### How can I use Blox?
You can use Blox’s scheduling capabilities from the Amazon ECS console, the ECS CLI, or SDK. The workflow will be very similar to the current workflow of using Amazon ECS.

##### What are the goals of Blox?
* Deliver a highly available, scalable, and performant set of schedulers for customers;
* Deliver schedulers as open source to enable additional extensibility and customization;
* Deliver schedulers as a managed service so customers do not need to manage or host critical infrastructure on their own;
* Enable customers to build and run the same schedulers that power Amazon ECS;
* Encourage transparent product feedback and community contributions.

##### What is the goal of Blox v1.0 compared to Blox v0.3?  
Customers wanted to see greater convergence across the open source Blox project and Amazon ECS schedulers, and asked for a managed or hosted option for Blox. Therefore, we are providing Blox as a managed option and making it available for use with Amazon ECS without having to manually install, deploy, and run it.

##### What are we doing with cluster state service? Can I continue to use it to build custom scheduling capabilities?
Blox provides an Event Stream Handler (cluster state service) that enables extensibility and it will continue to be available. We are looking for partner and customer feedback about their extensibility use cases as we decide on future investment into this service.

#### Can I use Blox to schedule containers with orchestrators besides Amazon ECS?
Not at the current time. Based on customer feedback, we built Blox using AWS primitives and it relies on the Amazon ECS control plane to run.

##### How can I extend Blox for my specific scheduling needs?   
We encourage contributions to Blox both in the form of features requests (see [Issues](https://github.com/blox/blox/issues)) and pull requests. All projects under Blox are released under Apache 2.0 and contributions are accepted under individual Apache Contributor Agreements.
