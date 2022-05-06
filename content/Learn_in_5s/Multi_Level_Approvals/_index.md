---
title: "Multi-Level Approvals"
weight: 500
---


Service Broker does provide various policy definitions and one of them can be used for Approvals of deployments and other actions within vRealize Automation. vRA Cloud and vRealize Automation 8.8 also provide capabilties to do Multi-Level Approvals, meaning more than one Level of approvals can be created. So for instance you may have one level of approval for deploying a catalog item and another level if the cost is above a certain amount, or if the resource sizes are above a certain threshold. 

Let's look at how this works.

### Setting Up the Policies

In the example below there are two policies:

 - Level 1 Policy - 
         Criteria: Deployment of Application Cloud Template
 - Level 2 Policy - 
         Criteria: Resources with Flavor: Large

Essentially the approvers that are assigned to the Level 1 Policy must first approve the request before the Level 2 Policy approvers will see the request. Once the Level 1 Policy has been approved, the request moves forward to the Level 2 approvers. Approval Policy levels can range between 1-99. 

The first level policy could look something like this:

{{< img src="level1pol.png">}}

The second (or next) level policy could look something like this:

{{< img src="level2pol.png">}}

The Approvers in the various level of policy can be chosen from various groups in the organization. So perhaps one level of policy may go to an administrator and then another level may go to a finance group for cost approval.



