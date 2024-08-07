# 42 NetPractice Project

Welcome to the 42 NetPractice project! This project is designed to enhance your networking skills through hands-on exercises that cover fundamental networking concepts. This README will guide you through key aspects of the project, including subnet masks, IP range calculations, and routing tables.

## Table of Contents

1. [Introduction](#introduction)
2. [Subnet Masks](#subnet-masks)
3. [IP Range Calculations](#ip-range-calculations)
4. [Routing Tables](#routing-tables)
5. [Installation and Setup](#installation-and-setup)
6. [Examples](#examples)
7. [Frequently Asked Questions (FAQ)](#frequently-asked-questions-faq)
8. [Contributing](#contributing)
9. [License](#license)

## Introduction

The NetPractice project will help you practice and master various essential networking concepts. Exercises cover subnet mask management, IP range calculation, and routing table analysis.

## Subnet Masks

### What is a Subnet Mask?

A subnet mask is used to divide an IP network into smaller subnetworks, allowing for more efficient IP address management. It is usually expressed in either CIDR (Classless Inter-Domain Routing) notation or dotted decimal notation.

### CIDR Notation

- **CIDR Notation**: /24, /16, /8, etc.
- **Example**: A /24 subnet mask means that the first 24 bits of the IP address are used for the network, and the remaining 8 bits are used for hosts.

### Subnet Mask Calculation

To convert a subnet mask from dotted decimal notation to binary notation, use the following formula:
- **CIDR Notation**: /24
- **Binary Mask**: 11111111.11111111.11111111.00000000
- **Decimal Mask**: 255.255.255.0

## IP Range Calculations

### IP Address Range

The IP address range of a subnet is determined by the network address, subnet mask, and broadcast address. Here's how to calculate them:

1. **Network Address**: The starting address of the subnet. This is the address obtained by setting all host bits to 0.
2. **Broadcast Address**: The ending address of the subnet. This is the address obtained by setting all host bits to 1.
3. **Host Range**: The range of usable addresses for hosts is between the network address and the broadcast address.

### Example Calculation

- **IP Address**: 192.168.1.10
- **Subnet Mask**: 255.255.255.0 (/24)
- **Network Address**: 192.168.1.0
- **Broadcast Address**: 192.168.1.255
- **Host Range**: 192.168.1.1 to 192.168.1.254

## Routing Tables

### What is a Routing Table?

A routing table is used by routers to determine the best path for forwarding packets to their destination. It contains information about accessible networks, available routes, and associated metrics.

### Structure of a Routing Table

- **Destination**: The network or IP address of the destination.
- **Subnet Mask**: The mask used for the destination.
- **Gateway**: The IP address of the next router to reach the destination.
- **Interface**: The network interface through which packets should be sent.
- **Metric**: A measure of distance or cost associated with the route.

### Example Routing Table

| Destination    | Subnet Mask          | Gateway      | Interface | Metric |
|----------------|-----------------------|---------------|-----------|--------|
| 192.168.1.0    | 255.255.255.0         | 0.0.0.0       | eth0      | 1      |
| 10.0.0.0       | 255.0.0.0             | 192.168.1.1   | eth1      | 2      |
| 0.0.0.0        | 0.0.0.0               | 192.168.1.1   | eth0      | 10     |
