# Software Defined Networks: Link Delay Measurement

## Overview

This is the final project for the "Software Defined Networks" course at Politecnico di Milano (2023/24). The goal of this project is to use a Ryu SDN controller to calculate real-time link delays between switches in a network.

## Key Features

* **Works Anywhere:** Supports any network topology as long as it has at least two interconnected switches.


* **Dynamic & Resilient:** Automatically adapts to network changes. You can plug or unplug switches on the fly without breaking the delay measurements.


* **Traffic-Aware:** Calculates delays based on actual network traffic and congestion, not just theoretical limits.


* **Data Visualization:** Automatically generates boxplots and probability density graphs of the network delays using Matplotlib.



## How It Works

The controller measures delay in a simple three-step process:

1. It estimates the baseline delay between the controller and the switches using `EchoRequest` and `EchoReply` messages.


2. It injects custom measurement packets into the network and records their departure time.


3. When the packets return, it calculates the exact travel time by subtracting the baseline delay from the arrival time.



## Technologies Built With

* **Python:** Core controller logic.


* **Ryu SDN Controller:** Framework for managing the network.


* **Mininet:** Used for network emulation.


* **Matplotlib:** Used for generating delay statistics and plots.


* *(Tested on physical hardware using Raspberry Pis and a Netgear switch)*.



## Authors

Pietro Ghersetich, Simone Francesco Curci, Marco Febbo, Amina El Kharouai

---

**Disclaimer:** *This project is for academic purposes only and is not intended for external testing or deployment.*
