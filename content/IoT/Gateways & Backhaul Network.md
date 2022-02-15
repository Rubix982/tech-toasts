---
title: "Gateways & Backhaul Network"
metaTitle: "Gateways & Backhaul Network"
metaDescription: "Gateways & Backhaul Network"
---

## The Core IoT Functional STack

Layers,

- "Things" Layer
  - At this layer, the physical devices need to fit
- Communications Network Layer
  - Access Network Sublayer
  - Gateways and backhaul network sublayer
  - Network Transport Sublayer
  - IoT Network Management SubLayer
    - CoAp, MQTT. If a sensor wants to send the temperature value as an integer. We can use CoAP, memory consumption, bandwidth usage
- Application And Analytics Layer,
  - How the end user should be able to use the end application
  - Let's say we make a stick for blind folks, how is it concerned to analytics? How should the end user think about it? We can have a beep message how the user will get the data and analytics out of it
  - Predictive analytics, bayesian and frequentist appproaches to how data can be used to predict te future
- Low Or High Reporting Frequency
- Simple Or Rich Data
- Report Range

## Mobility And Throughput

### High Mobility & High Throughput

### High Mobility & Low Throughput

### Low Mobility & High Throughput

### Low Mobility & Low Throughput

## Hybrid Approaches

Traditional plus new approaches.

What things do we need to get the setup initialized.

## Topologies

- Point-to-point topologies
  - Direct interaction
- Point-to-multipoint topologies
  - Sensors
  - Most IoT technologies where one or more than one gateways communicate with multiple smart objects are in this category
- Feasibility
  - Product launch, testing is done

Some examples are,

- Star Topology
- Clustered Stars

## Data Versus Network Analytics

Compute stack. The things tat are required here, which are required to perform the calculation and computation.

These new requirements include the following,

- Minimizing latency
- Conserving NEtwork Bandwidth
- Increasing Local Efficiency

## Fog Computing

The solution to the challenges mentioned in the previous section is to distribute data management throughout the IoT system, as close to the edge of the IP network as possible.

The best-known embodiment of edge services in IoT is fog computing.

Any device with computing, storage, and network connectivity can be a fog nodes.

Examples include industrial controllers, switches, routers, embedded servers and IoT gateways.

Analyzing IoT data close to where it is collected minimizes battery.

An advantage of this structure is that the fog node allows intelligence gathering (such as analytics) and control from the closest possible point, and in doing so, it allows better performance over constrained networks.

## High Latency, Low Latency

- Edge Layer (Low),
  - Embedded Systems and Sensors (Vehicles, Machines, etc)
- Fog Computing Layer (Medium),
  - Multi-Service Edge (IoT Gateway)
- Cloud Layer (High),
  - Core Data Center
