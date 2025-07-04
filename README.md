<h1>Layer 3 Spine-Leaf Data Center Network with OSPF and EtherChannel</h1>

<h2>Project Overview</h2>
This project is a simulation of a modern data center network using a spine-leaf architecture in Cisco Packet Tracer. The design consists of 2 spine switches and 3 leaf switches, all configured as Layer 3 switches to support high-performance routing across the topology.

The primary goal of this design is to demonstrate scalable, redundant, and efficient communication between endpoints in a data center environment.

Key features of the project include:

Spine-Leaf Architecture:
- Two spine switches serve as the high-speed backbone of the network.
- Three leaf switches act as access switches, each connecting to servers and the spines.
- Every leaf is connected to every spine to ensure non-blocking, low-latency communication.

Layer 3 Routing:
- All switches are configured for Layer 3 routing using OSPF (Open Shortest Path First).
- Routed point-to-point links are established between spines and leaves using no switchport interfaces.
- SVIs (Switched Virtual Interfaces) are configured for internal IP reachability.

EtherChannel (Port-Channel) Configuration:
- EtherChannel is implemented between leaf and spine switches to increase bandwidth, ensure redundancy, and enable load balancing.
- Multiple physical links are bundled into logical port-channels to prevent STP (Spanning Tree Protocol) blockages and improve throughput.

End Devices:
- Multiple servers are connected to the leaf switches to simulate real-world enterprise services.
- The design ensures that all servers can communicate through the spines via dynamic routing and port aggregation.

<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Project walk-through:</h2>
Starting off the project, we are provided an internet connection that simulates an ISP. 
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture2.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<br />
<br />
We begin by placing one router, five Layer 3 switches, and six servers onto the rack to form the core of our data center topology.  <br/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Each server will connect to ports F0/20 and F0/21 on the respective leaf switches. The spine-leaf network will be wired as follows:  <br/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture4.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
Completed wired setup for the network  <br/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
After activating the router interfaces, I assigned the appropriate IP addresses to enable network communication. <br/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next, OSPF was configured on the router to enable dynamic routing, followed by a connectivity test to verify communication with the ISP server (11.1.1.10)  <br/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next, we will configure Spine 1 and Spine 2 by enabling routing on interface G1/0/24 and setting up the OSPF protocol. A VLAN interface will also be configured on each spine to establish Layer 3 connectivity with the leaf switches  <br/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next, we will configure VLAN 1 on all leaf switches, assign IP addresses to their VLAN interfaces, and enable the OSPF routing protocol for dynamic route exchange with the spine switches.  <br/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture10.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture11.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture12.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next, we will configure EtherChannels across the network to aggregate links and improve redundancy and bandwidth. Below is the EtherChannel summary for the configured interfaces  <br/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture13.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture14.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture15.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture16.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture17.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture18.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
<br />
After assigning static IP addresses to all servers, we will perform a final connectivity test to verify end-to-end communication across the network. <br/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture19.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/jessies98/Networking1.2/blob/main/images/Picture20.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

