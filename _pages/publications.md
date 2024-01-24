---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can find my full publication list on my <i class="fas fa-fw fa-graduation-cap"> </i> <a href="{{author.googlescholar}}"> Google Scholar</a> profile.<br/>

# Overview of Recent Work

In network slicing, the customer and the network operator sign a service level agreement. This agreement specifies the QoS delivered to the network slice of the customer and the price that the customer needs to pay in exchange.

Notice that splitting the resources fairly between the slices means little to the customers if their share is not enough to deliver the promised QoS. Hence resource sharing schemes based on utility maximization are not enough. Resource provisioning mechanisms are also needed.

To estimate the required provisioned resources, the operator may monitor the resources that each slice needs over a long period of time, and then provision for each slice the largest amount of resources it requested.

This is simple to do but wasteful since the traffic of a slice varies over time. To enable dynamic resource adaptation for reduced provisioned resources, we propose the following architecture:


<img src="/images/system.svg" alt="Proposed Architecture">

* Bandwidth Demand Estimator: monitors online the traffic state of the network slice (number of users, number of queued bits, channel conditions, etc.) and outputs the number of resources needed to deliver the desired QoS.

* Network Slice Multiplexer: decides which bandwidth demands to accept if the provisioned resources are not enough to accept all of them.
