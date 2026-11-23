# **Module III – Applications of Queuing Theory in Computer Systems**

Final topic of Module III

## **1. Introduction**

Queuing Theory is used in computer systems to study how tasks, requests, data packets and processes wait for resources or services.

In a computer system, multiple requests may arrive at the same time, but the processor, memory, disk or network may not be able to handle all of them immediately. Queuing theory helps manage these waiting lines and improve system performance.

**Example:** When multiple applications request CPU time, the operating system places processes in queues and schedules them for execution.

## **2. Applications in Operating Systems**

An Operating System (OS) manages different processes and resources. Queuing theory helps the OS decide how processes wait and receive services.

### **A. CPU Scheduling**

- Multiple processes may request CPU time at the same time.
- The operating system maintains a ready queue for processes waiting for CPU execution.
- Scheduling algorithms select which process gets the CPU next.

**Example:** In FCFS scheduling, the process that enters the ready queue first gets CPU time first.

### **B. Disk Scheduling**

- Multiple processes may request data from the hard disk or SSD.
- These requests wait in a disk queue until the storage device processes them.
- Disk scheduling decides the order in which requests are handled.

**Example:** When multiple applications request files, the operating system manages their disk I/O requests.

### **C. Memory Management**

- Multiple processes require memory for execution.
- Memory requests may wait when sufficient memory is unavailable.
- Queuing concepts help understand and manage pending memory requests.

### **D. Process Management**

- Processes may wait for CPU, I/O devices or other resources.
- The OS maintains different queues, such as ready queues and waiting queues.
- These queues help manage process execution and resource allocation.

## **3. Applications in Computer Networks**

Queuing theory is widely used in computer networks because data packets arrive continuously and network devices need to process and forward them.

### **A. Router and Switch Queues**

- Routers receive data packets from different devices.
- If packets arrive faster than they can be forwarded, they wait in a buffer or queue.
- The router sends packets according to its scheduling policy.

**Example:** A router receives packets from multiple computers and places them in a queue before forwarding them.

### **B. Packet Transmission**

- Data is divided into small packets before transmission.
- Packets may have to wait before using a communication channel.
- Queuing theory helps calculate packet waiting time and transmission delay.

### **C. Network Congestion**

- Congestion occurs when too much data enters a network.
- Network devices may become overloaded, causing long queues and packet loss.
- Queuing theory helps analyze congestion and improve network performance.

### **D. Quality of Service (QoS)**

- QoS gives different priorities to different types of network traffic.
- Important traffic, such as voice and video calls, can receive higher priority.
- Priority queuing helps reduce delays for important data.

**Example:** During a video call, voice and video packets may be given higher priority than background downloads.

## **4. Other Applications in Computer Systems**

### **A. Web Servers**

- Many users send requests to a web server at the same time.
- Requests wait in a queue when the server is busy.
- Queuing theory helps estimate response time and server workload.

### **B. Printer Management**

- Multiple computers may send print requests to one printer.
- Print jobs are stored in a print queue.
- The printer processes the jobs one by one, usually following FCFS.

### **C. Database Management Systems**

- Multiple users may request data from a database simultaneously.
- Database operations may wait for CPU, disk access or locks.
- Queuing theory helps analyze transaction delays and system performance.

### **D. Cloud Computing**

- Multiple users send tasks to cloud servers.
- Tasks may wait until computing resources become available.
- Queuing theory helps manage workload distribution and resource utilization.

## **5. Advantages of Queuing Theory in Computer Systems**

1. **Reduces Waiting Time:** Helps reduce the time processes and requests spend waiting.
2. **Improves Resource Utilization:** Helps use CPU, memory, disks and network devices efficiently.
3. **Controls Congestion:** Helps identify and manage overloaded systems.
4. **Improves Performance:** Helps improve response time and overall system efficiency.
5. **Better Resource Allocation:** Helps distribute available resources among different requests.
6. **Supports System Design:** Helps estimate the resources required to handle expected workloads.

## **6. Summary Table**

| Computer system    | Application of queuing theory         |
| ------------------ | ------------------------------------- |
| Operating System   | CPU scheduling and process management |
| Disk Management    | Handling disk I/O requests            |
| Memory Management  | Managing pending memory requests      |
| Computer Networks  | Packet transmission and router queues |
| Network Congestion | Managing overloaded network traffic   |
| Web Servers        | Handling multiple user requests       |
| Printers           | Managing print jobs                   |
| Database Systems   | Managing database transactions        |
| Cloud Computing    | Managing incoming computing tasks     |

## **7. Conclusion**

Queuing theory plays an important role in computer systems by managing waiting requests and improving resource utilization. It is used in operating systems, computer networks, web servers, databases and cloud computing to reduce waiting time, control congestion and improve overall system performance.

## **Quick Revision 📝**

Remember these important connections for the exam:

- **CPU scheduling** → Ready queue.
- **Disk scheduling** → Disk request queue.
- **Router** → Packet queue.
- **Network congestion** → Too many packets waiting.
- **QoS** → Priority-based packet handling.
- **Web server** → User request queue.
- **Printer** → Print queue.
- **Cloud computing** → Task queue.

## **Important Exam Questions**

1. Explain the applications of queuing theory in operating systems.
2. Explain the applications of queuing theory in computer networks.
3. How is queuing theory useful in CPU scheduling and disk scheduling?
4. Explain the role of queuing theory in network congestion and QoS.
5. Discuss the applications and advantages of queuing theory in computer systems.


You have now covered all the topics in Module III, from the basics of queuing theory to M/M/1 analysis and computer-system applications.