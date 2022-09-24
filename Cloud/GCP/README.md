# Exam Guide

<details open><summary> <h2>Section 1. Applying site reliability engineering principles to a service</h2> </summary><blockquote>
    <details><summary><h3>1.1 Balance change, velocity, and reliability of the service:</h3></summary>
        <ol>
            <li>Discover SLIs (e.g., availability, latency)</li>
            <li>Define SLOs and understand SLAs</li>
            <li>Agree to consequences of not meeting the error budget</li>
            <li>Construct feedback loops to decide what to build next</li>
            <li>Eliminate toil via automation</li>
        </ol>
    </details>
    <details>
    <summary><h3>1.2 Manage service life cycle</h3></summary>
        <ol>
            <li>Manage a service (e.g., introduce a new service, deploy, </li>maintain, and retire it)
            <li>Plan for capacity (e.g., quotas and limits management)</li>
        </ol>
    </details>
    <details>
    <summary><h3>1.3 Ensure healthy communication and collaboration for operations</h3></summary>
        <ol>
            <li>Prevent burnout (e.g., set up automation processes to </li>prevent burnout)
            <li>Foster a learning culture</li>
            <li>Foster a culture of blamelessness</li>
        </ol>
    </details>
</details>

<details open><summary> <h2>Section 2. Building and implementing CI/CD pipelines for a service</h2> </summary><blockquote>
    <details><summary> <h3>2.1 Design CI/CD pipelines:</h3> </summary>
        <ol>
            <li>Creating and storing immutable artifacts with Artifact Registry</li>
            <li>Deployment strategies with Cloud Build and Spinnaker</li>
            <li>Deployment to hybrid and multicloud environments with Anthos, Spinnaker, and Kubernetes</li>
            <li>Artifact versioning strategy with Cloud Build and Artifact Registry</li>
            <li>CI/CD pipeline triggers with Cloud Source Repositories, external SCM, and Pub/Sub</li>
            <li>Testing a new version with Spinnaker</li>
            <li>Configuring deployment processes (e.g., approval flows)</li>
        </ol>
    </details>
    <details>
    <summary><h3>2.2 Implement CI/CD pipelines</h3></summary>
        <ol>
            <li>CI with Cloud Build</li>
            <li>CD with Cloud Build</li>
            <li>Open source tooling (e.g., Jenkins, Spinnaker, GitLab, Concourse)</li>
            <li>Auditing and tracing of deployments (e.g., CSR, Artifact Registry, Cloud Build, Cloud Audit Logs)</li>
        </ol>
    </details>
    <details>
    <summary><h3>2.3 Manage configuration and secrets</h3></summary>
        <ol>
            <li>Secure storage methods</li>
            <li>Secret rotation and config changes</li>
        </ol>
    </details>
    <details>
    <summary><h3>2.4 Manage infrastructure as code</h3></summary>
        <ol>
            <li>Terraform</li>
            <li>Infrastructure code versioning</li>
            <li>Make infrastructure changes safer</li>
            <li>Immutable architecture</li>
        </ol>
    </details>
    <details>
    <summary><h3>2.5 Deploy CI/CD tooling</h3></summary>
        <ol>
            <li>Centralized tools vs. multiple tools (single vs. multi-tenant)</li>
            <li>Security of CI/CD tooling</li>
        </ol>
    </details>
    <details>
    <summary><h3>2.6 Manage different development environments (e.g., staging, production)</h3></summary>
        <ol>
            <li>Decide on the number of environments and their purpose</li>
            <li>Create environments dynamically per feature branch with GKE</li>
            <li>Local development environments with Docker, Cloud Code, Skaffold</li>
        </ol>
    </details>
    <details>
    <summary><h3>2.7 Secure the deployment pipeline</h3></summary>
        <ol>
            <li>Vulnerability analysis with Artifact Registry</li>
            <li>Binary Authorization</li>
            <li>IAM policies per environment</li>
        </ol>
    </details>
</details>

<details open><summary><h2>Section 3. Implementing service monitoring strategies</h2> </summary><blockquote>
    <details><summary> <h3>3.1 Manage application logs:</h3> </summary>
        <ol>
            <li>Collecting logs from Compute Engine, GKE with Cloud Logging, Fluentd</li>
            <li>Collecting third-party and structured logs with Cloud Logging, Fluentd</li>
            <li>Sending application logs directly to the Cloud Logging API</li>
        </ol>
    </details>
    <details>
    <summary><h3>3.2 Manage application metrics with Cloud Monitoring</h3></summary>
        <ol>
            <li>Collecting metrics from Compute Engine</li>
            <li>Collecting GKE/Kubernetes metrics</li>
            <li>Use Metrics Explorer for ad hoc metric analysis</li>
        </ol>
    </details>
    <details>
    <summary><h3>3.3 Manage Cloud Monitoring platform</h3></summary>
        <ol>
            <li>Creating a monitoring dashboard</li>
            <li>Filtering and sharing dashboards</li>
            <li>Configure third-party alerting in Cloud Monitoring (e.g., PagerDuty, Slack)</li>
            <li>Define alerting policies based on SLIs with Cloud Monitoring</li>
            <li>Automate alerting policy definition with Terraform</li>
            <li>Implementing SLO monitoring and alerting with Cloud Monitoring</li>
            <li>Understand Cloud Monitoring integrations (e.g., Grafana, BigQuery)</li>
            <li>Using SIEM tools to analyze audit/flow logs (e.g., Splunk, Datadog)</li>
            <li>Design Cloud Monitoring metrics scopes</li>
        </ol>
    </details>
    <details>
    <summary><h3>3.4 Manage Cloud Logging platform</h3></summary>
        <ol>
            <li>Enabling data access logs (e.g., Cloud Audit Logs)</li>
            <li>Enabling VPC flow logs</li>
            <li>Viewing logs in the Google Cloud Console</li>
            <li>Using basic vs. advanced logging filters</li>
            <li>Implementing logs-based metrics</li>
            <li>Understanding the logging exclusion vs. logging export</li>
            <li>Selecting the options for logging export</li>
            <li>Implementing a project-level / org-level export</li>
            <li>Viewing export logs in Cloud Storage and BigQuery</li>
            <li>Sending logs to an external logging platform</li>
        </ol>
    </details>
    <details>
    <summary><h3>3.5 Implement logging and monitoring access controls</h3></summary>
        <ol>
            <li>Set ACL to restrict access to audit logs with IAM, Cloud Logging</li>
            <li>Set ACL to restrict export configuration with IAM, Cloud Logging</li>
            <li>Set ACL to allow metric writing for custom metrics with IAM, Cloud Monitoring</li>
        </ol>
    </details>
</details>

<details open><summary> <h2>Section 4. Optimizing service performance</h2> </summary><blockquote>
    <details><summary> <h3>4.1 Identify service performance issues:</h3> </summary>
        <ol>
            <li>Evaluate and understand user impact</li>
            <li>Utilize Google Cloud’s operations suite to identify cloud resource utilization</li>
            <li>Utilize Cloud Trace and Cloud Profiler to profile performance characteristics</li>
            <li>Interpret service mesh telemetry</li>
            <li>Troubleshoot issues with the image/OS</li>
            <li>Troubleshoot network issues (e.g., VPC flow logs, firewall logs, latency, view network details)</li>
        </ol>
    </details>
    <details>
    <summary><h3>4.2 Debug application code</h3></summary>
        <ol>
            <li>Application instrumentation</li>
            <li>Cloud Debugger</li>
            <li>Cloud Logging</li>
            <li>Cloud Trace</li>
            <li>Debugging distributed applications</li>
            <li>App Engine local development server</li>
            <li>Error Reporting</li>
            <li>Cloud Profiler</li>
        </ol>
    </details>
    <details>
    <summary><h3>4.3 Optimize resource utilization</h3></summary>
        <ol>
            <li>Identify resource costs</li>
            <li>Identify resource utilization levels</li>
            <li>Develop plan to optimize areas of greatest cost or lowest utilization</li>
            <li>Manage preemptible VMs</li>
            <li>Utilize committed use discounts where appropriate</li>
            <li>TCO considerations (e.g., security, logging, networking)</li>
            <li>Consider network pricing</li>
        </ol>
    </details>
</details>

<details open><summary> <h2>Section 5. Managing service incidents</h2> </summary><blockquote>
    <details><summary> <h3>5.1 Coordinate roles and implement communication channels during a service incident:</h3> </summary>
        <ol>
            <li>Define roles (incident commander, communication lead, operations lead)</li>
            <li>Handle requests for impact assessment</li>
            <li>Provide regular status updates, internal and external</li>
            <li>Record major changes in incident state (e.g., When mitigated? When is all clear?)</li>
            <li>Establish communications channels (e.g., email, IRC, Hangouts, Slack, phone)</li>
            <li>Scaling response team and delegation</li>
            <li>Avoid exhaustion / burnout</li>
            <li>Rotate / hand over roles</li>
        </ol>
    </details>
    <details>
    <summary><h3>5.2 Investigate incident symptoms impacting users:</h3></summary>
        <ol>
            <li>Identify probable causes of service failure</li>
            <li>Evaluate symptoms against probable causes; rank probability of cause based on observed</li>
            <li>Perform investigation to isolate most likely actual cause</li>
            <li>Identify alternatives to mitigate issue</li>
        </ol>
    </details>
    <details>
    <summary><h3>5.3 Mitigate incident impact on users</h3></summary>
        <ol>
            <li>Roll back release</li>
            <li>Drain / redirect traffic</li>
            <li>Turn off experiment</li>
            <li>Add capacity</li>
        </ol>
    </details>
    <details>
    <summary><h3>5.4 Resolve issues with deployments (e.g., Cloud Build, Jenkins)</h3></summary>
        <ol>
            <li>Code change / fix bug</li>
            <li>Verify fix</li>
            <li>Declare all-clear</li>
        </ol>
    </details>
    <details>
    <summary><h3>5.5 Document issue in a postmortem</h3></summary>
        <ol>
            <li>Document root causes</li>
            <li>Create and prioritize action items</li>
            <li>Communicate postmortem to stakeholders</li>
        </ol>
    </details>   
</details>
