![Customer Service Role in Incidents](assets/images/headers/CustServOps-Incidents.png)

> ...Customers don’t remember the actual incident, but rather the
experience during the disruption of their service. Customers expect software to fail, but
also expect that the experience the vendor provides them to be world-class.<br>
-- Manjula Talreja, Chief Customer Officer, PagerDuty

Customer service teams are a key participant in successful incident response. While digital organizations strive for proactive monitoring and telemetry collection across services and applications, complexity and scale make being perfectly proactive all but impossible. End users may notice something is wrong before an alarm triggers sometimes. Providing a clear path for customer service teams to escalate customer-reported issues to the appropriate teams, and to participate in the remediation process, focuses incident resolution on the customer.

Whether trouble is reported by end users and escalated via customer service, or reported by monitoring systems and reported to customer service, including customer service teams in incident response can strengthen customer relationships just when they are potentially weakened because of incidents. In the “old way of working,” customer service teams are left out of this workflow, exacerbating the chaos and confusion that occurs during an incident. When multiple disconnected customer service agents are hearing from customers, and creating duplicate tickets and reach outs, valuable time is wasted in both the identification and resolution of issues.

!!! tip
    Make your customer service/support team part of delivering customer satisfaction instead of just reporting on it.

## Aggregation of Customer-Reported Issues
When an incident triggers and a technical team is mobilized for response, they should know exactly what services are impacted, and hopefully know what the extent of the incident is. We refer to this as the “blast radius” of an incident. While this sounds scary, it is meant to be a measure of how much of the service is impacted, how many features, the depth to which they are affected, and discovering whether they are slow or completely offline. Today, it’s very hard for developers to determine customer impact. That's where customer service teams can help — they can help development understand customer impact by associating inbound customer complaints to technical incidents to help drive priorities.

Complex meshes of interconnected microservices make determining the blast radius of an incident difficult. If your team also practices other methodologies, such as A/B testing or canary deployments, not all users may be experiencing the same issues in the same way.

As a customer service team receives reports of issues during an incident, that data becomes part of the impact of the incident and should be incorporated into the resolution process. Some examples include:

- **Geographic aggregation**: “We’re seeing increased reports of issues from customers in central and southern Europe, but not northern Europe.”
- **Data partitioning**: “We’re seeing increased reports of issues for customers with account numbers starting with 1-4 only.”
- **Product versioning**: “We’re seeing increased reports of issues for customers on version 5.1 of the client software” or “customers using Android are reporting more problems than customers using iOS.”
- **Feature partitioning**: “Only accounts with the new Teapot Customization feature enabled are seeing issues.”

This is all vitally important intelligence that can be difficult to dig out of the services themselves, especially when application teams are trying to remediate the incident. Even when some of the data points might be known (e.g., the datacenter in southern Europe is offline — customer reports verify that your failover to another datacenter for those customers has failed).

Customer service teams will also have insight into whether an incident is improving or getting worse based on the number of customers reporting issues over time. This is important for cascading failures. For example, one geographic location failing may overload the next-closest location. It’s also vital information for identifying if a resolution is having the intended impact on the customer experience.

## Prioritization and SLAs
Your customer service team is in a unique position to help confirm the impact of an incident with regards to your end users. This is especially important when you have a contractual service level agreement (SLA) with your users, particularly if different customers might have different SLAs. Your customer service team will have the insight to know when your services are reaching their SLA for certain customers and alert the responding team. This is an important piece of information to manage, and engineering teams might not have the visibility into those contractual agreements.

Managing customer SLAs aids in the prioritization of issues during incidents, if restoring some services first will maintain an SLA for a customer or category of customers. Customer service can also advise on whether or not an incident should be escalated or have its severity increased based on the customer intelligence they are receiving. More customer impact could mean a higher severity level for the incident, more responders included in the triage, and more stakeholders informed.

## Customer Liaison and Stakeholder Communication
We’ve written about communications during incidents in some of our other [ops guides](https://pagerduty.com/ops-guides){:target="_blank" }. In the [Incident Response guide](https://response.pagerduty.com/training/customer_liaison/){:target="_blank" } there is a section on the Customer Liaison, and communicating with customers. We also have the [Stakeholder Communications](https://stakeholders.pagerduty.com/){:target="_blank" } guide that delves deeper into the specifics of communicating during an incident.

Your customer service team leaders are essential participants when it comes to codifying your communications practices for incidents. Customer service teams should be helping to create the messaging for customers, templatize responses, and manage communications channels.

Not all of your customers will be watching your social media accounts for updates, or even to verify if there is an issue going on with your services, before reporting to your support team. Communications from your customer service team during an incident should be built into templates with clear information about the services impacted and where to go for more information.

## Post-Incident Follow Up
Maintaining customer relationships after an incident is crucial. Incidents happen to everyone, all the time, and how your organization responds and communicates with customers afterwards will set you apart from other organizations.

Many customers will figure out when a service is restored and things are back to normal when they try to access the service, or if they are watching your status page or status updates. For customers that report issues, and for customers with priority support or other white glove services, your customer service team is there to reach out personally and let users know that the incident is over.

Depending on the nature of the services impacted and user interest, your customer service team may notify users when the services are verified to be restored, but they can also notify customers after the [postmortem](https://postmortems.pagerduty.com){:target="_blank" } is held. This gives the customer service team extra data to present to the users about the impact of the incident, the resolution, and the long-term plans for prevention. The customer service team follows the incident reports in a *full-case ownership* methodology, providing the customer with a consistent point of contact through issue resolution.

An incident that violates a contractual SLA definitely warrants a personal response from your organization, particularly if refunds or credits are due to impacted users. Even if the contractual obligations aren’t broken, customer service teams can identify users that might need additional attention, assurances, or incentives after an incident.
