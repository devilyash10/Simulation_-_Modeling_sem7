# **Module IV – Topic 4: Determining Events and Variables**

## **1. Introduction**

In discrete-event simulation, determining events and variables is an important step in developing a simulation model.

- **Events** are occurrences that cause a change in the state of a system.
- **Variables** are values used to represent and track the current condition of the system.

Before developing a simulation model, we must identify which events can occur and which variables are required to describe the system.

**Example:** In a bank, customer arrival and service completion are events, while the number of customers waiting and cashier status are variables.

## **2. Determining Events**

An event is an occurrence that changes the state of a system at a particular point in simulation time.

### **Steps to determine events**

1. **Study the system:** Understand how the real-world system works.
2. **Identify important activities:** Find activities that can change the system's condition.
3. **Identify state changes:** Determine what changes when each activity occurs.
4. **Define events:** Give names to the events that cause these changes.
5. **Determine event timing:** Identify when each event occurs.

### **Types of Events**

**1. Arrival Event**

- Occurs when a new entity enters the system.
- Example: A customer enters a bank or a packet arrives at a router.

**2. Departure Event**

- Occurs when an entity leaves the system.
- Example: A customer leaves after receiving service.

**3. Service Completion Event**

- Occurs when the processing or service of an entity is completed.
- Example: A cashier finishes serving a customer.

**4. Resource Failure Event**

- Occurs when a resource stops working.
- Example: A machine breaks down during production.

**5. Resource Repair Event**

- Occurs when a failed resource becomes operational again.
- Example: A technician repairs a machine.

## **3. Determining Variables**

Variables are used to represent the current state and performance of a simulation system. Their values may change during the simulation.

### **Types of Variables**

**1. State Variables**

- Describe the current condition of the system.
- They change when events occur.

Example:

- Number of customers in a queue.
- Number of busy machines.
- Current status of a server.

**2. Counter Variables**

- Keep track of the number of occurrences or completed activities.
- They are useful for collecting statistics.

Example:

- Total customers served.
- Number of machine failures.
- Total packets processed.

**3. Time Variables**

- Store time-related information about the simulation.
- They help calculate waiting time and service time.

Example:

- Current simulation time.
- Customer arrival time.
- Service completion time.

## **4. Example: Bank Simulation**

Consider a bank with one cashier and a waiting queue.

| Events               | Variables                    |
| -------------------- | ---------------------------- |
| Customer arrival     | Number of customers in queue |
| Service starts       | Cashier status               |
| Service completion   | Total customers served       |
| Customer departure   | Current number of customers  |
| Cashier becomes idle | Cashier idle time            |

### **Working of the System**

1. A customer arrives at the bank.
2. The number of customers in the system increases.
3. If the cashier is free, service starts; otherwise, the customer waits.
4. When service is completed, the customer departs.
5. The system updates its variables and waits for the next event.

## **5. Difference Between Events and Variables**

| Events                             | Variables                                       |
| ---------------------------------- | ----------------------------------------------- |
| Represent occurrences in a system. | Represent information about a system.           |
| Cause changes in system state.     | Store the current system state or other values. |
| Occur at specific points in time.  | May change during simulation.                   |
| Example: Customer arrival.         | Example: Number of customers waiting.           |
| Example: Service completion.       | Example: Cashier status.                        |

## **6. Importance of Determining Events and Variables**

1. Helps develop an accurate simulation model.
2. Identifies important changes in the system.
3. Helps track the system's current condition.
4. Makes event scheduling easier.
5. Helps collect and analyze simulation results.

## **Hinglish Explanation**

Is topic mein humein identify karna hota hai ki simulation ke andar **kaun-kaun se events honge aur unhe track karne ke liye kaun se variables chahiye.**

**Events:** Jo system mein koi change karte hain.

Example: Customer arrival, service start, service complete hona.

**Variables:** Jo system ki current information store karte hain.

Example: Queue mein kitne customers hain, cashier busy hai ya free, total kitne customers serve hue.

Easy trick:

- Event = Kya hua?
- Variable = Abhi system ki condition kya hai?

## **Quick Revision**

| Term             | Remember it as                       |
| ---------------- | ------------------------------------ |
| Event            | Occurrence that changes system state |
| State Variable   | Current system condition             |
| Counter Variable | Counts occurrences                   |
| Time Variable    | Stores time information              |
| Arrival Event    | Entity enters the system             |
| Departure Event  | Entity leaves the system             |



Exam tip

&#x20;Prepare the definition, types of events, types of variables, bank example and the difference table. These are the main points for a 10-mark answer.



**Next topic: Approaches for Time Advance.**