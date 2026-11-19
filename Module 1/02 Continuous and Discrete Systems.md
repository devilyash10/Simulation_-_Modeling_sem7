# **Module I – Introduction to Modeling and Simulation**

## **2. Continuous and Discrete Systems**

### **2.1 Introduction**

In simulation and modeling, systems are classified based on how their state changes over time. Two important types of systems are **Continuous Systems** and **Discrete Systems**.

A continuous system is one in which the system's state changes continuously with time, whereas a discrete system is one in which the system's state changes only at specific points in time.

Understanding these two systems is important because they require different approaches when creating simulation models.

### **2.2 Continuous System**

**Definition:**

A continuous system is a system in which the state variables change continuously with respect to time. This means that the values of the system can change at any instant, even if the changes are very small.

In continuous systems, changes generally occur gradually rather than at separate, identifiable event times. These systems are commonly represented using mathematical equations, especially differential equations.

**Examples:**

1\. **Water Level in a Tank:** The water level changes continuously as water enters or leaves the tank. Its height can be measured at any instant of time.

2\. **Temperature of a Room:** Room temperature changes gradually with time depending on heating, cooling and environmental conditions.

3\. **Movement of a Vehicle:** The position and speed of a moving vehicle can change continuously as time passes.

4\. **Electric Current:** Current and voltage in electrical circuits can vary continuously with time.

**Characteristics of Continuous Systems:**

- The state variables change continuously over time.
- Changes can occur at any instant of time.
- The system is generally represented using differential equations.
- Time is treated as a continuous variable.
- These systems are commonly used to represent physical processes.

### **2.3 Discrete System**

**Definition:**

A discrete system is a system in which the state variables change only at specific points or particular events in time. Between two consecutive events, the state of the system generally remains unchanged.

In these systems, changes occur when a particular event takes place. Discrete systems are commonly used to represent systems involving customers, machines, transactions and computer processes.

**Examples:**

1\. **Banking Queue:** The number of customers waiting in a bank changes whenever a customer arrives or leaves the queue.

2\. **Computer Network:** The number of packets in a network buffer changes when packets arrive or are transmitted.

3\. **Inventory System:** The quantity of products in a warehouse changes when new products arrive or existing products are sold.

4\. **Traffic Signal:** The traffic signal changes its state when a particular time interval is completed or a control event occurs.

**Characteristics of Discrete Systems:**

- The state variables change only at specific points in time.
- Changes occur due to particular events.
- The state generally remains constant between consecutive events.
- These systems are commonly represented using event-based simulation.
- They are widely used in banking, computer networks and manufacturing systems.

### **2.4 Difference Between Continuous and Discrete Systems**

| Basis            | Continuous System                              | Discrete System                                    |
| ---------------- | ---------------------------------------------- | -------------------------------------------------- |
| Meaning          | State variables change continuously with time. | State variables change at specific points in time. |
| Nature of change | Gradual and continuous.                        | Event-based or sudden.                             |
| Time             | Continuous time.                               | Events occur at separate time points.              |
| State            | Can change at any instant.                     | Generally remains constant between events.         |
| Representation   | Often uses differential equations.             | Often uses event-based models.                     |
| Examples         | Temperature, water level, vehicle movement.    | Bank queue, network packets, inventory.            |
| Applications     | Physical and engineering systems.              | Banking, manufacturing and computer systems.       |

### **2.5 Practical Example to Understand the Difference**

Consider two different situations:

**Situation 1 – Water Tank (Continuous System)**

Suppose water is continuously entering a tank through a pipe. The water level increases gradually with time. We can measure the water level at any instant, such as 1.5 seconds, 2.5 seconds or 3.5 seconds.

Therefore, the water level is a continuous state variable, making this a continuous system.

**Situation 2 – Bank Queue (Discrete System)**

Suppose customers arrive at a bank and wait for service. When a customer arrives, the number of customers in the queue increases. When a customer leaves, the number decreases.

The number of customers changes only when an arrival or departure event occurs. Therefore, this is a discrete system.

### **2.6 Important Points to Remember**

- Continuous systems have state variables that change continuously with time.
- Discrete systems have state variables that change at specific points in time.
- Differential equations are commonly used to represent continuous systems.
- Event-based simulation is commonly used to represent discrete systems.
- Water level and temperature are examples of continuous systems.
- Banking queues and computer network packet queues are examples of discrete systems.

### **2.7 Important Exam Questions**

1. Define continuous and discrete systems with suitable examples.
2. Differentiate between continuous and discrete systems.
3. Explain the characteristics of continuous and discrete systems.
4. Give real-world examples of continuous and discrete systems.

**Quick memory trick:**

- Continuous = Changes all the time (Water level, Temperature).
- Discrete = Changes when an event happens (Customer arrives, Packet leaves).

**Exam tip:** The difference between continuous and discrete systems is particularly suitable for a comparison question. Prepare the definition, at least four differences and two examples of each.