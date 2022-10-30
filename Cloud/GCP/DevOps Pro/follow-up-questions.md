## Questions

**What is fluentd?**
- Fluentd scraps logs from a given set of sources, processes them (converting into a structured data format) and then forwards them to other services like Elasticsearch, object storage etc

**What is a daemonset?**

- A DaemonSet ensures that all eligible nodes run a copy of a Pod. Normally, the node that a Pod runs on is selected by the Kubernetes scheduler. However, DaemonSet pods are created and scheduled by the DaemonSet controller instead

**What are scopes in GCP?**

- Access scopes are the legacy method of specifying authorization for your instance


**What is cloud platform scope?**

- IAM restricts access to APIs based on the IAM roles that are granted to the service account.
- Access scopes potentially further limit access to API methods.
- The best practice is to set the full cloud-platform access scope on the instance, then control the service account's access using IAM roles.

**What is syslog?**
- Syslog is an IETF RFC 5424 standard protocol for computer logging and collection 

**Difference between cluster autoscaler and horizontal pod scaling?**

- **Horizontal Pod autoscaler:** Allow to update the numbers of replicas of a targeted deployment. Based on a metric you specify (eg: CPU...). This only affect the numbers of pods (not the numbers of nodes).

- **Cluster autoscaler:** Allow to add new nodes to a nodepool if pods are not schedulables due to a lack a ressources (eg: CPU, memory...). This only affect the numbers of nodes (not the numbers of pods).

(Note that you can use both at the same Time)

**What is image digest?**
- A digest is an id that is automatically created during build time and cannot be changed (immutable)

**What are preemptible virtual machines and what is good use cases for them?**

- Spot instance equivalent in AWS, cheap instances that can be stopped anytime by Google 
- A Preemptible VM works best for applications or systems that distribute processes across multiple instances in a cluster

**What is kubectl builder?**

**What is web proxy logs?**
- A web proxy relays URL requests from clients to a server. Analysing web proxy logs can give unobtrusive insights to the browsing behavior of computer users and provide an overview of the Internet usage in an organization.
  
**What is Access Context Manager?**

- Access Context Manager allows enterprises to configure access levels which map to a policy defined on request attributes.

**When is an organizational policy used?**

 - The Organization Policy Service gives you centralized and programmatic control over your organization's cloud resources

**What is sample volume scale in VPC flow logs?**

- VPC Flow Logs records a sample of network flows sent from and received by VM instances, including instances used as Google Kubernetes Engine nodes. These logs can be used for network monitoring, forensics, real-time security analysis, and expense optimization

**What is container analysis?**

- Container Analysis is a service that provides vulnerability scanning and metadata storage for containers
  
**What is the difference between CPU usage and workload?**
-  Load is simply a count of the number of processes using or waiting for the CPU at a single point in time.
  

- For a single-CPU system, if the load is less than 1, that means on average, every process that needed the CPU could use it immediately without being blocked. Conversely, if the load is greater than 1, that means on average, there were processes ready to run, but could not due to CPUs being unavailable.

- Therefore, there’s a world of difference between 100% CPU usage and load = 1, and 100% CPU usage and load = 10.

- [Detailed Explanation](https://estl.tech/cpu-usage-vs-load-ecca22287b21)

**What is client instrumentation?**

- Client Instrumentation refers to software applications that enable remote management of a client system.