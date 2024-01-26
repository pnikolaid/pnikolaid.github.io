---
layout: archive
title: "Selected Work"
permalink: /selected-work/
author_profile: true
---

# Network Slicing

In network slicing, the customer and the network operator sign a service level agreement. This agreement specifies the QoS delivered to the network slice of the customer and the price that the customer needs to pay in exchange.

Notice that fairly splitting the resources between the slices means little to the customers if their share cannot deliver the promised QoS. Hence resource sharing schemes based on utility maximization are not enough. Resource provisioning mechanisms are also needed.

To estimate the required provisioned resources, the operator may monitor the resources that each slice needs over a long period of time, and then provision for each slice the largest amount it requested.

This is simple to do but wasteful since the traffic of a slice varies over time. To reduced the provisioned resources, we propose the following architecture that enables dynamic resource adaptation:
<br/>
<br/>

<img src="/images/system.svg" alt="Proposed Architecture">

**Bandwidth Demand Estimator**: monitors online the traffic of the slice and outputs the resources needed for the desired QoS

**Network Slice Multiplexer**: decides online which demands to accept if the provisioned resources are not enough for all

The previous architecture needs to be deployed at various nodes that compose the network slice. At the base station of a cellular network, the bandwidth demand corresponds to the physical resource blocks needed by the MAC scheduler of the slice to meet the desired QoS. At a switch, the bandwidth demand corresponds to the weight used by the PGPS algorithm running at its output ports. In the following two papers, we propose an implementation for each network function.

**Data-driven Bandwidth Adaptation for Radio Access Network Slices** <a href="https://arxiv.org/abs/2311.17347">  <i class="fas fa-solid fa-file"></i></a>
<br/>

<img align ="left" height="100" src="/images/testbed_site_4.png" alt="Testbed">
We developed a <ins>Bandwidth Demand Estimator</ins> that adapts the physical resource blocks allocated to each slice at a base station based on its traffic and packet delay requirements. Note that allocating few resources that are just enough to meet the desired QoS may create large packet queues and hinder the allocation process later on. For this reason, we proposed a Reinforment Learning approach that utilizes QoS feedback. We implemented the proposed algorithm on a 3GPP compliant testbed by Amarisoft. We were able to significantly reduce the average allocated bandwidth and improve the QoS delivery.
<br/>
<br/>

**Resource Efficiency vs Performance Isolation Tradeoff in Network Slicing** <a href="https://ieeexplore.ieee.org/document/10349807"> <i class="fas fa-solid fa-file"></i></a>
<br/>

<img  align="left" height="100" src="/images/multiplex_site_2.svg" alt="Tradeoff">
We developed a <ins>Network Slice Multiplexer</ins> that considers performance isolation. Although statistical multiplexing reduces the provisioned bandwidth, unexpected traffic surges in one slice may affect the other slices since the resources are being shared. To handle this tradeoff, we proposed the reservation of resources that are guaranteed to each slice no matter the traffic in other slices. Then, we found that the multiplexing policy that requires the least provisioned resources when the demands follow Markov Chains is the well-known Max-Weight scheduler. We investigated the tradeoff via experimentation on the LTE module of ns-3.





