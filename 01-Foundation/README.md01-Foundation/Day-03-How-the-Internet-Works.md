
📚 Day 03 – How the Internet Works
Part 1 – Internet Fundamentals

Module: Foundation
Day: 03/50
Difficulty: ⭐ Beginner
Estimated Reading Time: 15–20 Minutes

📖 Introduction

Every day we open websites like:

Google
Amazon
YouTube
LinkedIn
GitHub

It usually takes less than a second for these websites to load.

But have you ever wondered:

What actually happens after you type https://google.com into your browser?

Does your browser directly know where Google is?

Does your computer know Google's address?

How does your request travel from your laptop to Google's servers located thousands of kilometers away?

This chapter answers those questions.

By the end of this chapter, you will understand how the Internet works and why concepts like DNS, TCP, HTTPS, and Routing are essential for modern applications.

🎯 Learning Objectives

After completing this chapter, you will be able to:

Explain what the Internet is.
Understand the concept of a Network.
Differentiate between Packet Switching and Circuit Switching.
Understand the role of ISP, Router, and Switch.
Explain how data travels across the Internet.
Build a strong foundation for upcoming topics like DNS, TCP, and HTTPS.
🌍 What is the Internet?

Many beginners think:

Internet = Google ❌
Internet = Wi-Fi ❌
Internet = Browser ❌

None of these are correct.

Definition

The Internet is a global network of interconnected computer networks that communicate using the TCP/IP protocol suite.

Let's simplify this.

Imagine there are millions of separate networks around the world:

Your Home Wi-Fi
Your Office Network
Your College Network
Jio Network
Airtel Network
Google's Internal Network
Amazon AWS Network
Microsoft Azure Network

These networks are connected together.

That's why we call it:

Network of Networks

🌍 Real-World Analogy

Imagine India's road system.

Each city has its own roads:

Noida
Delhi
Kanpur
Lucknow
Mumbai

These cities are connected by highways.

This allows a vehicle to travel from Noida to Mumbai.

Similarly,

Every organization has its own network.

The Internet connects these independent networks together so computers can communicate worldwide.

🖥️ What is a Network?

A Network is a group of devices connected together so they can communicate and share resources.

Examples of devices:

Laptop
Mobile Phone
Printer
Smart TV
CCTV Camera
Server

These devices communicate using networking protocols.

Types of Networks
Type	Description	Example
LAN	Local Area Network	Home Wi-Fi
MAN	Metropolitan Area Network	City-wide network
WAN	Wide Area Network	Internet

For now, remember:

LAN → Small area
MAN → City
WAN → Country / World

The Internet is the world's largest WAN.

🧩 How Do Computers Communicate?

Imagine you upload a 100 MB video.

Question:

Does your laptop send the entire file as one huge block?

❌ No.

Instead, it breaks the file into many small pieces.

These small pieces are called:

Packets

📦 What is a Packet?

A Packet is the smallest unit of data transmitted over a network.

Instead of sending one large block of data, the Internet sends many packets.

Example:

100 MB File

↓

Packet 1

Packet 2

Packet 3

Packet 4

Packet 5

...

Packet N

Each packet travels independently.

At the destination, all packets are reassembled into the original file.

📦 What's Inside a Packet?

A packet contains more than just data.

Typical information includes:

Source IP Address
Destination IP Address
Sequence Number
Protocol Information
Payload (Actual Data)

Example:

Source IP:
192.168.1.10

Destination IP:
142.250.xxx.xxx

Payload:
Login Request

This information helps the network deliver packets correctly.

🔄 Packet Switching

The Internet uses a technique called Packet Switching.

Instead of reserving one fixed communication path, each packet can travel through different routes depending on network conditions.

Example:

Packet 1

↓

Router A

↓

Router B

↓

Destination


Packet 2

↓

Router C

↓

Router D

↓

Destination

Even if packets take different paths, they are reassembled correctly using sequence numbers.

Why Packet Switching?

Packet Switching provides several advantages:

Better bandwidth utilization
Faster communication
Fault tolerance
High scalability
No dedicated communication path required

If one route fails, another route can be used automatically.

This makes the Internet highly reliable.

☎️ Circuit Switching vs Packet Switching

Before the Internet, telephone systems used Circuit Switching.

A dedicated communication path was established between two users.

Example:

Person A
═══════════════
Dedicated Line
═══════════════
Person B

No one else could use that path until the call ended.

In contrast, Packet Switching dynamically chooses the best available path.

Circuit Switching	Packet Switching
Dedicated path	Dynamic path
Used in telephone systems	Used on the Internet
Less efficient	Highly efficient
Poor scalability	Highly scalable
🌐 Internet Service Provider (ISP)

Your laptop cannot directly connect to Google or Amazon.

It first connects to an Internet Service Provider (ISP).

An ISP provides Internet access.

Examples:

JioFiber
Airtel Xstream
BSNL
ACT Fiber
Excitel

Without an ISP, your device cannot access the Internet.

High-Level Communication Flow
Laptop
   │
   ▼
Home Router
   │
   ▼
ISP
   │
   ▼
Internet
   │
   ▼
Google / Amazon Network

Notice that your request does not directly jump to Google.

It passes through multiple networks.

📡 What is a Router?

A Router connects different networks together.

Its primary job is to determine the best path for forwarding packets.

Think of it as a traffic police officer.

It looks at the destination IP address and decides where the packet should go next.

Without routers, the Internet would not exist.

Responsibilities of a Router
Connects different networks
Routes packets
Maintains routing information
Chooses the best available path
Connects your home network to the Internet
🔀 What is a Switch?

A Switch connects devices within the same Local Area Network (LAN).

Example:

Laptop
     │
Printer
     │
Smart TV
     │
Office Server
     │
Switch

Unlike a router, a switch does not connect different networks.

It connects devices inside the same network.

Router vs Switch
Router	Switch
Connects different networks	Connects devices within the same network
Uses IP Address	Uses MAC Address
Layer 3 Device	Layer 2 Device
🌍 Real Production Example

Imagine you search:

https://amazon.in

At a high level:

Laptop

↓

Home Router

↓

ISP

↓

Regional ISP Network

↓

National Internet Backbone

↓

Amazon Network

↓

Amazon Server

This journey takes only a few milliseconds.

In the next part, we'll see how your browser actually finds Amazon's IP address using DNS, because at this stage the browser only knows the domain name (amazon.in), not the server's IP address.

📝 Key Takeaways
The Internet is a Network of Networks.
Devices communicate using networking protocols.
Data is transmitted in the form of Packets.
The Internet uses Packet Switching.
Routers connect different networks.
Switches connect devices within the same network.
ISPs provide Internet connectivity.
Your browser cannot directly reach Google or Amazon without the Internet infrastructure.
