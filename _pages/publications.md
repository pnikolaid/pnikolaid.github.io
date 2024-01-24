---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can find my full publication list on my <i class="fas fa-fw fa-graduation-cap"> </i> <a href="{{author.googlescholar}}"> Google Scholar</a> profile.<br/>
In what follows, I briefly describe my most recent work on network slicing. <br/>

In network slicing, the customer and the network operator sign a service level agreement. This agreement specifies the QoS delivered to the network slice of the customer and the price that the customer needs to pay in exchange.

In this paradigm, sharing the resources fairly between the slices means little to the customers if their promised QoS is violated. Hence resource sharing schemes based on utility maximization are not enough. Resource provisioning mechanisms are also needed.

We consider that the operator needs to monitor the resources that each slice needs over a long period of time. Based on these data, the operator may then provision resources accordingly to ensure the fulfillment of all the agreements.

largest amount of resources that each slice requested. Although this is simple to do, it is quite wasteful. Since the traffic of different slices varies over time, so does their resource demand. So it is beneficial to consider statistic multiplexing to reduce the required provisioned resources.
<img src="/images/system.svg" alt="Proposed Architecture">
