---
title: "Data Analytics, Business Benefits, Smart Services"
metaTitle: "Data Analytics, Business Benefits, Smart Services"
metaDescription: "Data Analytics, Business Benefits, Smart Services"
---

## Table Of Contents

- [Table Of Contents](#table-of-contents)
- [Data Analytics, Business Benefits, Smart Services](#data-analytics-business-benefits-smart-services)
- [Smart Services](#smart-services)
- [IoT Data Management & Compute Stack](#iot-data-management--compute-stack)
  - [Minimizing Latency](#minimizing-latency)
  - [Conserving Network Bandwidths](#conserving-network-bandwidths)
  - [Increasing Local Efficiency](#increasing-local-efficiency)
  - [The Traditional IT Cloud And Computing Model](#the-traditional-it-cloud-and-computing-model)
- [Fog Computing](#fog-computing)
- [Edge Computing](#edge-computing)

## Data Analytics, Business Benefits, Smart Services

- Almost any object can be connected, multiple types of sensors can be installed on a given object
- A smarter architectural choice may be to allow for an open system where the network is engineered to be flexible enough that other sensors may be added in the future
- Enhanced data processing can result in new added value for businesses that are not envisioned at the time when the system is initially developed
- This type of alert is a time saver, and avoids the need for the repair team to our all the machines in turn when only one may be malfunctioning

## Smart Services

- Smart Services use IoT, and aim for efficiency
- For example, sensors can be installed on equipment to ensure ongoing conformance with regulation or safety requirements
- Smart Services can also be used to measure the efficiency of machine by detecting machine output, speed, or other forms of usage evaluation
- Presence and motion sensors can evaluate the number of guests in a lobby and redirect personnel accordingly

## IoT Data Management & Compute Stack

In most cases, the processing location is outside the smart object. Smart objects need to connect to the cloud, and data processing is centralized. One advantage of this model is simplicity.

This model has limitations. These requirements tend to bring the need for data analysis closer to the IoT system.

### Minimizing Latency

Analyzing data close to the device that collected the data can make a difference between averting disaster and a cascading system failure

### Conserving Network Bandwidths

It is not practical to transport vast amounts of data from thousands or hundreds of thousands of edge devices to the cloud.

It is not even necessary because many critical analyses does not require cloud-scale processing and storage.

### Increasing Local Efficiency

The environmental conditions in one area will trigger a local response independent from the condition of another site hundreds of miles away.

### The Traditional IT Cloud And Computing Model

(Data Center/Cloud) <-> (Core Network) <-> (Endpoints)

The Traditional IT Cloud Computing Model

- **Data Center/Cloud**
- **Core Network**
- **Endpoints**

## Fog Computing

(Data Center/Cloud) <-> (Core IPv6 Network) <-> (Fog Layer) <-> (Smart Objects)

The best-known embodiment of edge services in **IoT** is **Fog Computing**. Any device with computing, storage, and network connectivity can be a fog node.

Analyzing IoT data to where it is collected minimizes latency, offloads gigabytes of network traffic from the core network, and keeps sensitive data inside the local network.

- **Data Center/Cloud**: (Hundreds) Data Center/Cloud, transactional response times
- **Core IPv6 Network**: (Thousands) Backhaul
- **Fog Layer**: (Tens Of Thousands) Multi-service Edge
- **Smart Objects**: (Millions) Embedded Systems And Sensors, Low Power, Low Bandwidth

## Edge Computing

- In recent years, the concepts of IoT computing has been pushed even further to the edge, and in some cases, it now resides directly
- Edge compute-capable meters are able to communicate with each other to share information on small subsets of the electrical distribution grid to monitor localized power quality and consumption
- Models such as these help ensure the highest quality of power delivery to customers
