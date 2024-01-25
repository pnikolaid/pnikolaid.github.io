---
layout: archive
title: "Selected Work"
permalink: /selected-work/
author_profile: true
---

# Network Slicing

In network slicing, the customer and the network operator sign a service level agreement. This agreement specifies the QoS delivered to the network slice of the customer and the price that the customer needs to pay in exchange.

Notice that splitting the resources fairly between the slices means little to the customers if their share is not enough to deliver the promised QoS. Hence resource sharing schemes based on utility maximization are not enough. Resource provisioning mechanisms are also needed.

To estimate the required provisioned resources, the operator may monitor the resources that each slice needs over a long period of time, and then provision for each slice the largest amount of resources it requested.

This is simple to do but wasteful since the traffic of a slice varies over time. To reduced the provisioned resources, we propose the following architecture that enables dynamic resource adaptation:

<img src="/images/system.svg" alt="Proposed Architecture">

**Bandwidth Demand Estimator**: monitors online the current traffic of the network slice and outputs the amount of resources currently needed to deliver the desired QoS

**Network Slice Multiplexer**: decides online which bandwidth demands to accept if the provisioned resources are not enough to accept all of them

The previous architecture needs to be deployed at various nodes that compose the network slice. At a base station of a cellular network, the bandwidth demand corresponds to the physical resource blocks needed by the MAC scheduler of the network slice to meet the desired QoS. At a switch, the demand may correspond to the weights used by the PGPS algorithm running at its output ports. In the following two papers, we propose an implementation for each network function.