# **Module V – Choice of Paths in GPSS**

## **1. Definition**

**Choice of Paths** in GPSS refers to the process of selecting different routes or paths through which a transaction can move during simulation.

A transaction may follow different paths depending on certain conditions, resource availability or selection rules.

**Example:** In a bank, customers may choose Counter 1 or Counter 2 depending on which counter is free.

## **2. Why is Choice of Paths Used?**

1. To represent different routes in a system.
2. To handle multiple service options.
3. To make simulation models more realistic.
4. To distribute transactions among different resources.
5. To model decision-making situations.

## **3. Types of Path Selection**

**1. Unconditional Path Selection**

- A transaction follows a fixed path without checking any condition.
- It moves from one block to another in a predefined order.

*Example:* Every customer follows the same route: arrival → queue → service → departure.

**2. Conditional Path Selection**

- A transaction selects a path based on a particular condition.
- The next path depends on whether the condition is satisfied.

*Example:* If Counter 1 is free, the customer goes to Counter 1; otherwise, the customer goes to Counter 2.

**3. Random Path Selection**

- A transaction selects one of several available paths randomly.
- The selection is based on a random choice or probability.

*Example:* Customers are randomly assigned to Counter 1 or Counter 2.

## **4. Example of Choice of Paths**

Suppose a bank has two service counters. Customers can be sent to either counter.

**Customer Arrival**

**Path Selection**

**Counter 1**

Service

**Counter 2**

Service

**Customer Departure**

The customer is directed to one of the counters according to the selected path.

## **5. Importance of Choice of Paths**

1. **Flexibility:** Allows transactions to follow different routes.
2. **Better Resource Utilization:** Helps distribute work among multiple resources.
3. **Realistic Modelling:** Represents real-world decision-making.
4. **Performance Improvement:** Helps avoid unnecessary waiting and delays.
5. **Complex System Modelling:** Makes it easier to represent systems with multiple activities.

## **6. Conclusion**

Choice of Paths in GPSS allows transactions to follow different routes during simulation. It is useful for modelling systems with multiple counters, machines, processes and decision-making conditions.

## **Quick Revision 📝**

| Term            | Meaning                             |
| --------------- | ----------------------------------- |
| Choice of Paths | Selecting a route for a transaction |
| Unconditional   | Fixed path                          |
| Conditional     | Path selected based on a condition  |
| Random          | Path selected randomly              |

**Remember:** Choice of Paths = Different routes for transactions.

## **Important Exam Questions**

1. Define Choice of Paths in GPSS.
2. Explain different types of path selection with examples.
3. Explain the importance of Choice of Paths in simulation.
4. Explain Choice of Paths with a suitable diagram.


## **Choice of Paths in GPSS – Important Questions**

### **Q1. Define Choice of Paths in GPSS.**

**Exam Answer:**

Choice of Paths in GPSS refers to selecting different routes through which a transaction can move during simulation. The path may depend on conditions, resource availability or random selection.

**Hinglish Summary:** Transaction ko simulation mein kis route se bhejna hai, us route ko select karna Choice of Paths kehlata hai.

### **Q2. Explain different types of path selection.**

**Exam Answer:**

1. **Unconditional Path:** A transaction follows a fixed path without checking any condition.
2. **Conditional Path:** A transaction selects a path based on a specific condition.
3. **Random Path:** A transaction selects one of the available paths randomly.

**Hinglish Summary:**

- Unconditional = Fixed route.
- Conditional = Condition ke according route.
- Random = Randomly route select hota hai.

### **Q3. Explain the importance of Choice of Paths in GPSS.**

**Exam Answer:**

1. Provides flexibility in simulation models.
2. Helps distribute work among multiple resources.
3. Represents real-world decision-making.
4. Improves resource utilization.
5. Helps model complex systems.

**Hinglish Summary:** Isse transactions ko different routes milte hain, workload distribute hota hai aur resources ka better use hota hai.

### **Q4. Explain Choice of Paths with an example.**

**Exam Answer:**

Consider a bank having two service counters. When a customer arrives, the simulation model selects Counter 1 or Counter 2. The customer follows the selected path, receives service and then leaves the system.

This represents Choice of Paths in GPSS.

**Hinglish Summary:** Bank mein do counters hain. Customer ko kisi ek counter par bhejna path selection ka example hai.

**Going forward:** I'll keep the English answer concise and add a Hinglish summary immediately below each answer.
**Next topic: Conditional Transfers in GPSS.**