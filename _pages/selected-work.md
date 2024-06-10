---
layout: archive
title: "Selected Work"
permalink: /selected-work/
author_profile: true
---

# Network Slicing

In network slicing, the customer and the network operator sign a service level agreement. This agreement specifies the QoS delivered to the network slice of the customer and the price that the customer needs to pay in exchange.

Here fairly splitting the resources between the slices means little to the customers if their share cannot deliver the promised QoS. As a result, resource sharing mechanisms based on utility maximization are not enough. Resource provisioning mechanisms are also needed.

To efficiently meet the QoS requirements of all slices, we propose the following architecture that enables dynamic resource adaptation:
<br/>
<br/>

<img src="/images/system.svg" alt="Proposed Architecture" width="900">

**Bandwidth Demand Estimator**: monitors online the traffic of the slice and outputs the amount of required resources

**Network Slice Multiplexer**: decides online which demands to accept if the provisioned resources are not enough for all

The previous architecture needs to be deployed at various nodes that compose the network slice. At the base station of a cellular network, the bandwidth demand corresponds to the physical resource blocks needed by the MAC scheduler of the slice to meet the desired QoS. At a switch, the bandwidth demand may correspond to the weight used by the PGPS algorithm running at its output ports. Also, the Network Slice Multiplexer should be provisioned with enough resources to be able to accept all the bandwidth demands for a high fraction of time. In the following papers, we propose implementations for each network function.

**Data-driven Bandwidth Adaptation for Radio Access Network Slices** <a href="https://arxiv.org/abs/2311.17347">  <i class="fas fa-solid fa-file"></i></a>
<br/>

<img align ="left" height="100" src="/images/testbed_site_4.png" alt="Testbed">
We develop a <ins>Bandwidth Demand Estimator</ins> that adapts the physical resource blocks allocated to each slice at a base station based on its traffic and packet delay requirements. Note that allocating few resources that are just enough to meet the desired QoS may create large packet queues and hinder the allocation process later on. For this reason, we propose a Reinforment Learning approach that utilizes QoS feedback. We implement the proposed algorithm on a 3GPP compliant testbed by Amarisoft. We significantly reduce the average allocated bandwidth and improve the QoS delivery even for tail delay requirements.
<br/>
<br/>

**Resource Efficiency vs Performance Isolation Tradeoff in Network Slicing** <a href="https://ieeexplore.ieee.org/document/10349807"> <i class="fas fa-solid fa-file"></i></a>
<br/>

<img  align="left" height="100" src="/images/multiplex_site_2.svg" alt="Tradeoff">
We develop a <ins>Network Slice Multiplexer</ins> that considers performance isolation. Although statistical multiplexing reduces the provisioned bandwidth, unexpected traffic surges in one slice may affect the other slices since the resources are being shared. To handle this tradeoff, we propose the reservation of resources that are guaranteed to each slice no matter the traffic in other slices. Then, we find that the multiplexing policy that requires the least provisioned resources is the well-known Max-Weight scheduler if the demands follow Markov Chains. We investigate the tradeoff via experimentation on the LTE module of ns-3.
<br/>
<br/>

**Robust Resource Sharing via Hypothesis Testing** <a href="https://arxiv.org/abs/2404.18254"> <i class="fas fa-solid fa-file"></i></a>
<br/>

<img  align="left" height="100" src="/images/trial2.jpg" alt="Trial">
We propose the introduction of hypothesis testing in resource sharing to handle the tradeoff between efficiency and isolation without exclusive resource reservation. Our approach comprises two phases. In the trial phase, the operator obtains a stochastic model for each slice that describes its normal behavior, provisions resources and signs the service level agreements. In the regular phase, whenever there is resource contention, hypothesis testing is conducted to check which slices follow their normal behavior. Slices that fail the test are excluded from resource sharing to protect the well-behaved ones. Results show that our approach fortifies the service level agreements against unexpected traffic patterns with reduced resources.




