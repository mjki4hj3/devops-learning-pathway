# Exam Guide

<details><summary> <h2>Section 1. Applying site reliability engineering principles to a service</h2> </summary><blockquote>
    <details><summary> <h3>1.1 Balance change, velocity, and reliability of the service:</h3> </summary>
        1. Discover SLIs (e.g., availability, latency)
        2. Define SLOs and understand SLAs
        3. Agree to consequences of not meeting the error budget
        4. Construct feedback loops to decide what to build next
        5. Eliminate toil via automation
    </details>
    <details>
    <summary>1.2 Manage service life cycle:</summary>
        1. Manage a service (e.g., introduce a new service, deploy, maintain, and retire it)
        2. Plan for capacity (e.g., quotas and limits management)
    </details>
    <details>
    <summary>1.3 Ensure healthy communication and collaboration for operations:</summary>
        1. Prevent burnout (e.g., set up automation processes to prevent burnout)
        2. Foster a learning culture
        3. Foster a culture of blamelessness
    </details>
</details>

<details><summary> <h2>Section 2. Building and implementing CI/CD pipelines for a service</h2> </summary><blockquote>
    <details><summary> <h3>2.1 Design CI/CD pipelines:</h3> </summary>
        1. Creating and storing immutable artifacts with Artifact Registry
        2. Deployment strategies with Cloud Build and Spinnaker
        3. Deployment to hybrid and multicloud environments with Anthos, Spinnaker, and Kubernetes
        4. Artifact versioning strategy with Cloud Build and Artifact Registry
        5. CI/CD pipeline triggers with Cloud Source Repositories, external SCM, and Pub/Sub
        6. Testing a new version with Spinnaker
        7. Configuring deployment processes (e.g., approval flows)
    </details>
    <details>
    <summary><h3>2.2 Implement CI/CD pipelines</h3></summary>
        1. CI with Cloud Build
        2. CD with Cloud Build
        3. Open source tooling (e.g., Jenkins, Spinnaker, GitLab, Concourse)
        4. Auditing and tracing of deployments (e.g., CSR, Artifact Registry, Cloud Build, Cloud Audit Logs)
    </details>
    <details>
    <summary><h3>2.3 Manage configuration and secrets</h3></summary>
        1. Secure storage methods
        2. Secret rotation and config changes
    </details>
    <details>
    <summary><h3>2.4 Manage infrastructure as code</h3></summary>
        1. Terraform
        2. Infrastructure code versioning
        3. Make infrastructure changes safer
        4. Immutable architecture
    </details>
    <details>
    <summary><h3>2.5 Deploy CI/CD tooling</h3></summary>
        1. Centralized tools vs. multiple tools (single vs. multi-tenant)
        2. Security of CI/CD tooling
    </details>
    <details>
    <summary><h3>2.6 Manage different development environments (e.g., staging, production)</h3></summary>
        1. Decide on the number of environments and their purpose
        2. Create environments dynamically per feature branch with GKE
        3. Local development environments with Docker, Cloud Code, Skaffold
    </details>
    <details>
    <summary><h3>2.7 Secure the deployment pipeline</h3></summary>
        1. Vulnerability analysis with Artifact Registry
        2. Binary Authorization
        3. IAM policies per environment
    </details>
</details>

<details><summary><h2>Section 3. Implementing service monitoring strategies</h2> </summary><blockquote>
    <details><summary> <h3>3.1 Manage application logs:</h3> </summary>
        1. Collecting logs from Compute Engine, GKE with Cloud Logging, Fluentd
        2. Collecting third-party and structured logs with Cloud Logging, Fluentd
        3. Sending application logs directly to the Cloud Logging API
    </details>
    <details>
    <summary><h3>3.2 Manage application metrics with Cloud Monitoring</h3></summary>
        1. Collecting metrics from Compute Engine
        2. Collecting GKE/Kubernetes metrics
        3. Use Metrics Explorer for ad hoc metric analysis
    </details>
    <details>
    <summary>3.3 Manage Cloud Monitoring platform:</summary>
        1. Creating a monitoring dashboard
        2. Filtering and sharing dashboards
        3. Configure third-party alerting in Cloud Monitoring (e.g., PagerDuty, Slack)
        4. Define alerting policies based on SLIs with Cloud Monitoring
        5. Automate alerting policy definition with Terraform
        6. Implementing SLO monitoring and alerting with Cloud Monitoring
        7. Understand Cloud Monitoring integrations (e.g., Grafana, BigQuery)
        8. Using SIEM tools to analyze audit/flow logs (e.g., Splunk, Datadog)
        9. Design Cloud Monitoring metrics scopes
    </details>
    <details>
    <summary><h3>3.4 Manage Cloud Logging platform</h3></summary>
        1. Enabling data access logs (e.g., Cloud Audit Logs)
        2. Enabling VPC flow logs
        3. Viewing logs in the Google Cloud Console
        4. Using basic vs. advanced logging filters
        5. Implementing logs-based metrics
        6. Understanding the logging exclusion vs. logging export
        7. Selecting the options for logging export
        8. Implementing a project-level / org-level export
        9. Viewing export logs in Cloud Storage and BigQuery
        10. Sending logs to an external logging platform
    </details>
    <details>
    <summary><h3>3.5 Implement logging and monitoring access controls</h3></summary>
        1. Set ACL to restrict access to audit logs with IAM, Cloud Logging
        2. Set ACL to restrict export configuration with IAM, Cloud Logging
        3. Set ACL to allow metric writing for custom metrics with IAM, Cloud Monitoring
    </details>
</details>

<details><summary> <h2>Section 4. Optimizing service performance</h2> </summary><blockquote>
    <details><summary> <h3>4.1 Identify service performance issues:</h3> </summary>
        1. Evaluate and understand user impact
        2. Utilize Google Cloud’s operations suite to identify cloud resource utilization
        3. Utilize Cloud Trace and Cloud Profiler to profile performance characteristics
        4. Interpret service mesh telemetry
        5. Troubleshoot issues with the image/OS
        6. Troubleshoot network issues (e.g., VPC flow logs, firewall logs, latency, view network details)
    </details>
    <details>
    <summary><h3>4.2 Debug application code</h3></summary>
        1. Application instrumentation
        2. Cloud Debugger
        3. Cloud Logging
        4. Cloud Trace
        5. Debugging distributed applications
        6. App Engine local development server
        7. Error Reporting
        8. Cloud Profiler
    </details>
    <details>
    <summary><h3>4.3 Optimize resource utilization</h3></summary>
        1. Identify resource costs
        2. Identify resource utilization levels
        3. Develop plan to optimize areas of greatest cost or lowest utilization
        4. Manage preemptible VMs
        5. Utilize committed use discounts where appropriate
        6. TCO considerations (e.g., security, logging, networking)
        7. Consider network pricing
    </details>
</details>

<details><summary> <h2>Section 5. Managing service incidents</h2> </summary><blockquote>
    <details><summary> <h3>5.1 Coordinate roles and implement communication channels during a service incident:</h3> </summary>
        1. Define roles (incident commander, communication lead, operations lead)
        2. Handle requests for impact assessment
        3. Provide regular status updates, internal and external
        4. Record major changes in incident state (e.g., When mitigated? When is all clear?)
        5. Establish communications channels (e.g., email, IRC, Hangouts, Slack, phone)
        6. Scaling response team and delegation
        7. Avoid exhaustion / burnout
        8. Rotate / hand over roles
    </details>
    <details>
    <summary><h3>5.2 Investigate incident symptoms impacting users:</h3></summary>
        1. Identify probable causes of service failure
        2. Evaluate symptoms against probable causes; rank probability of cause based on observed
        3. Perform investigation to isolate most likely actual cause
        4. Identify alternatives to mitigate issue
    </details>
    <details>
    <summary><h3>5.3 Mitigate incident impact on users</h3></summary>
        1. Roll back release
        2. Drain / redirect traffic
        3. Turn off experiment
        4. Add capacity
    </details>
    <details>
    <summary><h3>5.4 Resolve issues with deployments (e.g., Cloud Build, Jenkins)</h3></summary>
        1. Code change / fix bug
        2. Verify fix
        3. Declare all-clear
    </details>
    <details>
    <summary><h3>5.5 Document issue in a postmortem</h3></summary>
        1. Document root causes
        2. Create and prioritize action items
        3. Communicate postmortem to stakeholders
    </details>   
</details>
