# **Module III – Introduction to Queuing Theory**

## **Topic 5: Queuing Disciplines**

### **1. What is a Queuing Discipline?**

**Definition:** Queuing Discipline is the rule that decides the order in which customers receive service in a queuing system.

In simple words, it tells us **who will be served first and who will have to wait.**

For example, in a bank, the customer who arrives first is usually served first. This is called FCFS.

### **2. Types of Queuing Disciplines**

There are four commonly used queuing disciplines:

### **1. FCFS – First Come, First Served**

In this method, the customer who arrives first gets served first.

**Example:** 🏦

In a bank, customers stand in a line. The person who arrives first receives service first.

**FCFS Example**

1st

Customer A

Served first

2nd

Customer B

3rd

Customer C

**Uses:** Banks, ticket counters and supermarkets.

### **2. LCFS – Last Come, First Served**

In this method, the customer who arrives last gets served first.

**Example:** 📚

Imagine a pile of books. The book placed last on top is picked up first.

Similarly, the last customer entering the system gets service first.

**Uses:** Stack-based systems and certain storage or processing arrangements.

### **3. SIRO – Service in Random Order**

In this method, customers are selected randomly for service. Their arrival order does not matter.

**Example:** 🎟️

Suppose five people are waiting for a lucky draw. Any one of them can be selected randomly, regardless of when they arrived.

**Uses:** Random selection systems and certain communication systems.

### **4. Priority Queuing**

In this method, customers are served according to their importance or priority rather than their arrival time.

**Example:** 🚑

In a hospital, emergency patients are treated before patients with minor health problems.

**Uses:** Hospitals, emergency services and computer operating systems.

### **3. Types of Priority Queuing**

Priority queuing can be divided into two types:

**A. Preemptive Priority**

In this method, a high-priority customer can interrupt the service of a low-priority customer.

*Example:* An emergency patient arrives while a normal patient is receiving treatment. The doctor stops the normal treatment to handle the emergency.

**B. Non-Preemptive Priority**

In this method, once service starts, it is completed before another customer can be served, even if a higher-priority customer arrives.

*Example:* A bank employee completes the current customer's transaction before serving a priority customer.

### **4. Difference Between Queuing Disciplines**

| Discipline | Service Rule                    | Example            |
| ---------- | ------------------------------- | ------------------ |
| FCFS       | First arrival served first      | Bank queue         |
| LCFS       | Last arrival served first       | Stack of books     |
| SIRO       | Random customer selected        | Lucky draw         |
| Priority   | Important customer served first | Hospital emergency |

### **5. Importance of Queuing Disciplines**

1. **Proper Service Order:** Defines how customers receive service.
2. **Time Management:** Helps manage customer waiting time.
3. **Priority Handling:** Allows important or emergency customers to receive faster service.
4. **System Efficiency:** Helps organise the service process.
5. **Better Resource Management:** Helps servers handle customers systematically.

### **6. Quick Revision 📝**

**Remember these four rules:**

- FCFS = First customer comes, first customer served.
- LCFS = Last customer comes, first customer served.
- SIRO = Any customer can be selected randomly.
- Priority = Most important customer served first.

**Priority types:**

- Preemptive = Service can be interrupted.
- Non-Preemptive = Current service cannot be interrupted.

### **7. Important Exam Questions**

1. Define Queuing Discipline and explain its different types.
2. Explain FCFS, LCFS and SIRO with examples.
3. What is Priority Queuing? Explain its types.
4. Differentiate between preemptive and non-preemptive priority.
5. Compare different queuing disciplines.



Exam tip

&#x20;For a 10–14 marks answer, write the definition, explain all four disciplines with examples, include the comparison table and explain both types of priority queuing.



**Next topic: Simulation of Single-Server Queue** — we'll understand how a queue with one service counter is simulated, step by step.
