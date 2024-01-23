---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can find my full publication list on my <i class="fas fa-fw fa-graduation-cap"> </i> <a href="{{author.googlescholar}}"> Google Scholar</a> profile.<br/>
In what follows, I briefly describe my last two papers on network slicing. <br/>

In network slicing, the customer and the network operator sign a service level agreement. This agreement specifies the QoS that the operator needs to deliver to the network slice of the customer. It also specifies the price that the customer needs to pay in exchange.

Due to these agreements, we argue that splitting the resources between network slices solely based on utility maximization schemes is not enough. Indeed, splitting resources based on proportional or max-min fairness means little to the customers. Their only concern is to receive the promised QoS that they are paying for.

Instead, the operators needs to first monitor the resources that each network slice needs over time. Based on these data, they can estimate the required provsioned resources and charge each customer accordingly.

For example, the operator may provision the maximum amount of resources needed by each network slice after monitoring it for a long period of time. Although this is simple to do, it is quite wasteful. Indeed, the traffic of different slices varies over time and so does their resource demand. So it is beneficial to consider statistic multiplexing to reduce the required provisioned resources.
<img src="/images/system.svg" alt="Proposed Architecture">
