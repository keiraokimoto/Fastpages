---
toc: true
comments: true
layout: post
title: Computers and Networks (Unit 4)
description: Add Definitions from Unit 4 Computer Systems and Networks
---

## Requirements
> Work through College Board Unit 4... blog, add definitions, and pictures.  Be creative, for instance make a story of Computing and Networks that is related to your PBL experiences this year.

### How a Computer Works
> As we have learned, a computer needs aa program to do something smart.  The sequence of a program initiates a series of actions with the computers Central Processing Unit (CPU). This component is essentially a binary machine focussing on program instructions provided.  The CPU retrieives and stores the data it acts upon in Random Access Memory (RAM). Between the CPU, RAM, and Storage Devices a computer can work with many programs and large amounts of data.

List specification of your Computer, or Computers if working as Pair/Trio
- Processor GHz: 2.7 GHz
- Memory in GB: 15.7 GB
- Storage in GB: 475 GB
- OS:22621.1413

Define or describe usage of Computer using Computer Programs. Pictures are preferred over a lot of text.  Use your experience.
- Input devices - hardware devices that allow the user to input data or commands into the computer
- Output devices  - hardware devices that allow the computer to display or output data 
- Program File - a file that contains a program or set of instructions that the computer can execute
- Program Code - the set of instructions that the computer reads and executes to perform a specific task
- Processes - programs that are currently running on the computer
- Ports - hardware components that allow the computer to communicate with other devices
- Data File - a file that contains data that is used by a program
- Inspect Running Code - the process of examining the code that is currently running on the computer, which can be done with debuggers
- Inspect Variables - the process of examining the values of variables that are currently in use by a program, which can be done using debugging tools and print statements

![Computer Hardware]({{site.baseurl}}/images/cpu.jpeg)

### The Internet
> Watch/review College Board Daily Video for 4.1.1

- Essential Knowledge
    - A computing device is a physical artifact that can run a program. Some examples include computers, tablets, servers, routers, and smart sensors.
    - A computing system is a group of computing devices and programs working together for a common purpose.
    - A computer network is a group of interconnected computing devices capable of sending or receiving data.
    - A computer network is a type of computing system. 
    - A path between two computing devices on a computer network (a sender and a receiver) is a sequence of directly connected computing devices that begins at the sender and ends at the receiver.
    - Routing is the process of finding a path from sender to receiver.
    - The bandwidth of a computer network is the maximum amount of data that can be sent in a fixed amount of time.
    - Bandwidth is usually measured in bits per second

- Complete Vocabulary Matching Activity. Incorporate this into your learnings from the year. To analyze measure path and latency use `traceroute` and `ping` commands from Linux Terminal.  
    - Path - the route or location of a file or folder on a computer or network, consists of a sequence of directory or folder names that indicate the location of the file or folder in a file system
    - Route - a route refers to the path or sequence of devices that a packet of data must traverse to reach its destination on a computer network, involves determining the optimal path for data to travel between network nodes
    - Computer System - a collection of hardware, software, and data that work together to perform specific tasks or functions, including components such as the central processing unit (CPU), memory, storage devices, input/output devices, and software applications.
    - Computer Device - any physical component of a computer system that is used to input, process, store, or output data, such as keyboards, mice, printers, monitors, and storage devices
    - Bandwidth - the amount of data that can be transmitted over a network connection in a given amount of time, usually measured in bits per second (bps) or bytes per second (Bps) and is often used to describe the speed of an internet connection or the capacity of a network
    - Computer Network - a collection of interconnected computers and devices that communicate with each other to share resources and exchange data. Networks can be small and local, such as a home network, or large and global, such as the internet, that can be wired or wireless, and can use a variety of different protocols and technologies to transmit data

    Path - A
    Route - E
    Computer System - B
    Computer Device - C 
    Bandwidth - D
    Computer Network - F

> Watch/review College Board Daily Video 4.1.2
- Complete True of False Questions

- Essential Knowledge
    - The internet is a computer network consisting of interconnected networks that use standardized, open (nonproprierary) communication protocols.
    - Access to the internet depends on the ability to connect a computing device to an internet connected device.
    - A protocol is an agreed-upon set of rules that specify the behavior of a system.
    - The protocols used in the internet are open, which allows users to easily connect additional computing devices to the internet.
    - Routing on the internet is usually dynamic; it is not specified in advance
    - The scalability of a system is the capacity for the system to change in size and scale to meet new demands.
    - The internet was designed to be scalable
    - Information is passed through the internet as a data stream. Data streams contain chunks of data, which are encapsulated in packets. 
    - Packets contain a chunk of data and metadata used for routing the packet between the origin and the destination on the internet, as well as for data reassembly.
    - Packets may arrive at the destination in order, out of order, or not at all
    - IP, TCP and UDP are common protocols used on the internet.
    - The world wide web is a system of linked pages, programs, and files.
    - HTTP is a protocol used by the world wide web
    - The world wide web uses the internet
    
    [T] Open standards and protocols enable different manufacturers and developers to build hardware and software on the rest of the internet.
    [F] Tor is a task force used to enforce laws to keep manufacturers out of the internet.
    [F] Routes are determined in advanced and are not flexible.
    [T] A protocol is an agreed-upon set of rules that specify the behavior of a system.
    [F] UDP guarantees transfers and is faster.
    [F] The World Wide Web is the internet.
    [T] HTTP is a protocol used by the World Wide Web.

- Go over AP videos, vocabulary, and essential knowledge. Draw a diagram showing the internet and its many levels. A preferred diagram would using your knowledge of frontend, backend, deployment, etc. Picture would highlight vocabulary by illustration. The below illustration have some ideas.

![Diagram]({{site.baseurl}}/images/Copy of Light Pink Minimalist Simple Quote Motivation Poster (1).png)

![Full Stack]({{site.baseurl}}/images/fullstack.png)

- Often we draw pictures of machines communicating over the Internet with arrows.  However, the real communication goes through protocol layers and the machine and then is trasported of the network.   For College Board and future Computer Knowledge you should become familiar with the following ...

```
     User Machine  <---> Frontend Server <---> Backend Server
    +-----------+         +-----------+         +-----------+
    |  Browser  |         |  GH Page  |         |   Flask   |
    +-----------+    ^    +-----------+    ^    +-----------+
    |    HTTP   |    |    |    HTTP   |    |    |    HTTP   |
    +-----------+    |    +-----------+    |    +-----------+
    |    TCP    |    |    |    TCP    |    |    |    TCP    |   
    +-----------+    |    +-----------+    |    +-----------+
    |     IP    |    V    |     IP    |    V    |     IP    |
    +-----------+         +-----------+         +-----------+
    |  Network  |  <--->  |  Network  |  <--->  |  Network  |
    +-----------+         +-----------+         +-----------+
```

The "http" layer is an application layer protocol in the TCP/IP stack, used for ***communication between web browsers and web servers***. It is the protocol used for transmitting data over the World Wide Web.

The "transport" layer (TCP) is responsible for providing reliable data transfer between applications running on different hosts.  The TCP protocol segments the data into smaller ***chunks called "segments"***. Each segment contains a sequence number that identifies its position in the original stream of data, as well as other control information such as source and destination port numbers, and checksums for error detection.

The "ip" layer is responsible for packetizing data received from the TCP layer of the protocol stack, and then ***encapsulating the data into IP packets***. The IP packets are then sent to the lower layers of the protocol stack for transmission over the network.

The "network" layer is responsible for ***routing data packets between networks*** using the Internet Protocol (IP). This layer handles tasks such as packet addressing and routing, fragmentation and reassembly, and ***network congestion*** control.

### Fault Tolerance
> Watch both Daily videos for 4.2
- Complete the network activity, summarize your understanding of fault tolerance.
  - Fault tolerence is the amount of tolerance a system of networks has to any breaks or disconnections in the system. For example, if one connection is severed, the device can still communicate with other devices in the network, because there are still connections to other devices. 

  Which of the following is NOT a benefit of a fault-tolerant network?
    A. Data has more than one path to travel from one device to another.
    B. If part of the network fails, the network can still function by using other paths.
    C. Data will only take one route from one device to another, no matter the number of routes available.
    D. More devices creates more connections and makes the network stronger.

    [C] Data will only take one route from one device to another, no matter the number of routes available.

  What would make this network fault-tolerant?
    A. A connection from A to B 
    B. A connection from B to C 
    C. A connection from E to G 
    D. A connection from E to F

    [A] A connection from A to B 

### Parallel and Distributed Computing
> Review previous lecture on Parallel Computing and watch Daily vidoe 4.3. Think of ways to make something in you team project to utilize Cores more effectively. Here are some thoughts to add to your story of Computers and Networks...

- What is naturally Distributed in Frontend/Backend archeticture?  
  - Naturally districuted frontend/backend architecture handles complex logic required for a program to run. This can include database, authentication, security management, and otherwise. User interfaces, inputs, and some other basic processes are part of the frontend, whereas data management and other application logic and tasks are distributed to the backend. 

- Analyze this command in Docker: ```ENV GUNICORN_CMD_ARGS="--workers=1 --bind=0.0.0.0:8086"```. Determine if there is options are options in this command for parallel computing within the server that runs python/gunicorn. Here is an [article](https://medium.com/building-the-system/gunicorn-3-means-of-concurrency-efbb547674b7)

> Last week we discussed parallel computing on local machine.  There are many options.  Here is something to get parallel computing work with a tool called Ray.
- Review this [article](https://www.anyscale.com/blog/writing-your-first-distributed-python-application-with-ray)...  Can you get parallel code on images to work more effectively?  I have not tried Ray.

- Code example from ChatGPT using squares. This might be more interesting if nums we generated to be a lot bigger.

```python
import ray

# define a simple function that takes a number and returns its square
def square(x):
    return x * x

# initialize Ray
ray.init()

# create a remote function that squares a list of numbers in parallel
@ray.remote
def square_list(nums):
    return [square(num) for num in nums]

# define a list of numbers to square
nums = [1, 2, 3, 4, 5]

# split the list into two parts
split_idx = len(nums) // 2
part1, part2 = nums[:split_idx], nums[split_idx:]

# call the remote function in parallel on the two parts
part1_result = square_list.remote(part1)
part2_result = square_list.remote(part2)

# get the results and combine them
result = ray.get(part1_result) + ray.get(part2_result)

# print the result
print(result)

```