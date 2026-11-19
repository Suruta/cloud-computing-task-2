Cloud computing task 2

This report focuses on the various ways organizations ensure the availability and reliability of cloud infrastructure, the significance of these metrics in the context of business continuity, the types of disruption that can occur in the cloud and the strategic design patterns used to counteract these risks.

Businesses rely heavily on data and the need for it to be reliable and available.
Reliability and availability are two concepts that are closely related and are essential for the success of a business. Availability is the percentage of time that a system is running and available to respond to requests; typically expressed as "nines". For example, 99.999% (Five 9s) availability equates to merely 5 minutes of allowable downtime per year. Reliability, on the other hand, is the likelihood that a system will work properly for a given set of conditions (Shunmugasundaram, 2018a). An available system is not reliable if it gives an error or corrupted data.

In the business world, high availability and reliability go hand in hand with revenue protection, customer trust and brand reputation. Outages in critical applications like e-commerce sites or financial services can lead to significant financial losses and irreparable reputational damage. Moreover, data durability, that is, the assurance that data does not disappear, is important. When these metrics are met, organizations can keep operating at full speed without having to deal with frequent system instability.

Disruptions, Infrastructure Failures, and External Threats.
Cloud environments, while robust, are not immune to disruptions. Organizations need to plan for all manner of failure – infrastructure failure is no exception (Sinclair, 2019). Common disruptions include:
1. Infrastructure Failures: Hardware failures, power outages or network partitioning in a specific AZ or geographic region.
2. Deployment Failures: Bugs or dependency issues due to software updates, configuration changes, or certificate expiration.
External Threats: Distributed Denial of Service attacks, malicious intrusions or third-party API failures.
4. Load Spikes: Unexpected heavy loads that overload the resources of the system and can cause cascading failures if not handled (Shunmugasundaram, 2018b).

To ensure availability and minimize risk, strategies are implemented.
These risks are addressed and businesses continued through a mix of architectural design patterns, operational automation, and extensive testing, in addition to shifting from fragile, monolithic systems to resilient, distributed systems.

Architectural Design Patterns
Multiple AZs, or geographic regions, help to ensure that failures in a single zone do not cause the failure of the entire system. For example, a 99.99% availability target might require deployment in three AZs and spread out capacity (Shunmugasundaram, 2018c).
The circuit breaker pattern is used to stop requests from a failing dependency from causing a cascade of failures.The circuit breaker pattern is used to prevent cascading failures when a dependency becomes difficult to access. The bulkhead pattern partitions each component of the system (such as ship's compartments) and makes sure that if one compartment runs out of resources, the entire application will not be affected (Shunmugasundaram, 2018b).
Queue Based Load Leveling and Throttling: Absorbing traffic peaks with asynchronous message queues, processes can work at a sustainable pace. Throttling restricts the amount of resources used on each user, ensuring that the essential services are maintained in case of high load (Shunmugasundaram, 2018b).
- Retry and Compensating Transactions: Transient network errors are addressed through idempotent, exponential backoff retries. In a distributed workflow, compensating transactions can roll back partial successes in the event of failure at a later stage, guaranteeing eventual consistency (Shunmugasundaram, 2018b).

Define Operational Excellence and Automation.Explain what Operational Excellence and Automation are.
Zero-Downtime Deployments: With Blue-Green or Canary deployments, organizations can deploy updates gradually and rollback if the key performance indicators are not meeting expectations (Shunmugasundaram, 2018a).
Complete Monitoring and Health Checks: Health endpoint monitoring is not limited to the web server, but also checks for downstream components such as databases and third-party APIs. Aggregated logging and real-time alerting allows teams to identify and address anomalies before customers are affected (Shunmugasundaram, 2018a).
Chaos Engineering and Failure Injection: Inject failure (such as killing instances) proactively to ensure that automated recovery mechanisms (such as Auto Scaling Groups replacing instances when they are in the unhealthy state) are working as expected (Shunmugasundaram, 2018a).

Conclusion
There is more to high availability and reliability in the cloud than just buying the high-end service; it demands a mindset change in architectural design and how services are operated. The best is not always 100% availability, but rather a calculated compromise between velocity, reliability, and cost. Resiliency is created by intentional redundancy, intelligent design patterns, and automated recovery.

Organizations need to embrace a cloud mindset, design for failure from day one. Implement multi-AZ deployments as a rule, ensure automated CI/CD pipelines with roll back functionality and ensure full health checks that include deep dependency monitoring, not just uptime monitoring.

Other research opportunities involve the use of AI and Machine Learning in predictive anomaly detection and autonomous self-healing systems to further minimize MTTR. Further, the environmental footprint and cost optimisation of multi-region active-active designs requires further study.

## references

DED (Data Engineering Digest) (2020) ‘Availability vs Reliability vs Durability vs Resiliency vs Fault tolerance’, Medium, 24 April. Available at: https://dataengineering-digest.medium.com/availability-vs-reliability-vs-durability-vs-resiliency-dfead8c92c58

Shunmugasundaram, S. (2018a) ‘Architecting for Reliability Part 1 — Concepts’, becloudy, Medium, 28 January. Available at: https://medium.com/becloudy/architecting-for-reliability-part-1-concepts-17028343089

Shunmugasundaram, S. (2018b) ‘Architecting for Reliability Part 2 — Resiliency and Availability Design Patterns for the Cloud’, becloudy, Medium, 30 January. Available at: https://medium.com/becloudy/architecting-for-reliability-part-2-resiliency-and-availability-design-patterns-for-the-cloud-cf7aaaed0df2

Shunmugasundaram, S. (2018c) ‘Architecting for Reliability Part 3 — High Availability Architectures’, becloudy, Medium, 23 March. Available at: https://medium.com/becloudy/architecting-for-reliability-part-3-high-availability-architectures-8dfd0f87d25e

Sinclair, I. (2019) ‘Availability & Reliability — how cloud changes the game’, google-cloud-jp, Medium, 11 December. Available at: https://medium.com/google-cloud-jp/availability-reliability-how-cloud-changes-the-game-e04aa0d56f00