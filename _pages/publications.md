---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can find my full publication list on my <i class="fas fa-fw fa-graduation-cap"> </i> <a href="{{author.googlescholar}}"> Google Scholar</a> profile.<br/>
In what follows, I briefly describe my most recent work on network slicing. <br/>

In network slicing, the customer and the network operator sign a service level agreement. This agreement specifies the QoS delivered to the network slice of the customer and the price that the customer needs to pay in exchange.

In this paradigm, the main concern of the customers is to receive the QoS that they are paying for. Indeed, splitting resources based on a fairness criterion means little to the customers if the promised QoS is violated. So it is necessary to consider resource provisioning mechanisms and not just utility maximization schemes to satisfy the previous agreements.

Instead, the operators needs to first monitor the resources that each network slice needs over time. Based on these data, they can estimate the required provsioned resources and charge each customer accordingly.

For example, the operator may provision the maximum amount of resources needed by each network slice after monitoring it for a long period of time. Although this is simple to do, it is quite wasteful. Indeed, the traffic of different slices varies over time and so does their resource demand. So it is beneficial to consider statistic multiplexing to reduce the required provisioned resources.
<img src="/images/system.svg" alt="Proposed Architecture">
