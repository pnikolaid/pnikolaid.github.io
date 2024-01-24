---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can find my full publication list on my <i class="fas fa-fw fa-graduation-cap"> </i> <a href="{{author.googlescholar}}"> Google Scholar</a> profile.<br/>
In what follows, I briefly describe my most recent work on network slicing. <br/>

In network slicing, the customer and the network operator sign a service level agreement. This agreement specifies the QoS delivered to the network slice of the customer and the price that the customer needs to pay in exchange.

In this paradigm, splitting resources based on a fairness criterion means little to the customers if the promised QoS is violated. Hence resource splitting mechanisms based on utility maximization are not enough. Resource provisioning mechanisms are also needed.

The operator needs to monitor the resources that each slice needs a long period of time. Based on these data, the operator may provision the sum of the largest amount of resources that each slice requested. Although this is simple to do, it is quite wasteful. Since the traffic of different slices varies over time, so does their resource demand. So it is beneficial to consider statistic multiplexing to reduce the required provisioned resources.
<img src="/images/system.svg" alt="Proposed Architecture">
