## cloude services

### key take aways to pivot

- How does the organizations keep availability and reliability of cloud infrastructure ?
- The importance of reliability and data availability for businesses
- Disruptions, infrastructure failures, external threats for cloud
- How does the organizations reduce these risks and maintain business


## What did I google

`medium cloud infrastructure availability reliability`  
`medium cloud reliability availability businesses`  
`medium cloud disruptions infrastructure failures threats`

## tools that was used

sublime text for IDE
markdown
chatgpt for web search

## links

https://medium.com/google-cloud-jp/availability-reliability-how-cloud-changes-the-game-e04aa0d56f00
https://dataengineering-digest.medium.com/availability-vs-reliability-vs-durability-vs-resiliency-dfead8c92c58

https://medium.com/becloudy/architecting-for-reliability-part-1-concepts-17028343089
https://medium.com/becloudy/architecting-for-reliability-part-2-resiliency-and-availability-design-patterns-for-the-cloud-cf7aaaed0df2
https://medium.com/becloudy/architecting-for-reliability-part-3-high-availability-architectures-8dfd0f87d25e

https://aws.amazon.com/architecture/well-architected/

## paragraphs

### 1

Traditional High Availability (HA) and Disaster Recovery (DR) models often relied on over-provisioned, idle failover infrastructure, resulting in high costs and periodic maintenance downtime (Sinclair, 2019).

### 2

### 3

For example, 99.999% (Five 9s) availability equates to merely 5 minutes of allowable downtime per year (Shunmugasundaram, 2018a). Reliability, however, is the probability that a system will function correctly as designed under specified conditions (DED, 2020).

### 4

Achieving these metrics ensures that organizations can maintain operational velocity without being bogged down by constant system instability (Sinclair, 2019).

### 5

Organizations must anticipate a wide array of failure modes, treating infrastructure failure as a given rather than an exception (Sinclair, 2019).

4. Load Spikes: Unexpected surges in traffic that overwhelm system resources, leading to cascading failures if not properly managed (Shunmugasundaram, 2018b).

### 6

### 7

For instance, a 99.99% availability target often requires deploying across three AZs with distributed capacity (Shunmugasundaram, 2018c).

The bulkhead pattern isolates system components (like compartments in a ship) so that resource exhaustion in one area does not sink the entire application (Shunmugasundaram, 2018b).

Throttling limits resource consumption per user, preserving core functionality for critical operations during extreme load (Shunmugasundaram, 2018b)

For complex distributed workflows, compensating transactions undo partial successes if a subsequent step fails, ensuring eventual consistency (Shunmugasundaram, 2018b).

### 8

- Zero-Downtime Deployments: Utilizing Blue-Green or Canary deployment strategies allows organizations to roll out updates incrementally, enabling immediate rollback if key performance indicators degrade (Shunmugasundaram, 2018a).

Aggregated logging and real-time alerting ensure that teams detect and resolve anomalies before customers are impacted (Shunmugasundaram, 2018a)

- Chaos Engineering and Failure Injection: Proactively testing systems by injecting failures (e.g., terminating instances) validates that automated recovery procedures, such as Auto Scaling Groups replacing unhealthy nodes, function as intended (Shunmugasundaram, 2018a).

### 9

The optimal goal is not an unrealistic 100% availability, but a calculated trade-off between velocity, reliability, and cost (Sinclair, 2019).

### 10

### 11

### 12







