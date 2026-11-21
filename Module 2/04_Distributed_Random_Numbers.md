# **Module II – Probability Concepts in Simulation**

## **Topic 4: Distributed Random Numbers**

### **1. What are Distributed Random Numbers?**

In simulation, we use random numbers to represent uncertain events such as customer arrivals, waiting times, machine failures and traffic movement.

**Distributed random numbers** are random numbers generated according to a particular probability distribution.

In simple words, these numbers are not always generated with equal chances. Their chances of occurring depend on the selected probability distribution.

### **2. Simple Example 🎲**

Suppose we generate random numbers between 1 and 6.

If every number has an equal chance of appearing, the numbers follow a **Uniform Distribution**.

But suppose we generate numbers according to a Normal Distribution. Values near the average will occur more frequently than values far from the average.

This means different distributions produce different patterns of random numbers.

### **3. Types of Distributed Random Numbers**

Random numbers can be generated according to different probability distributions.

**1. Uniformly Distributed Random Numbers**

- Every value within a given range has an equal chance of occurring.
- Example: Generating random numbers between 0 and 1.
- Used when all possible values are equally likely.

**2. Normally Distributed Random Numbers**

- Values near the average occur more frequently.
- Very high and very low values occur less frequently.
- Example: Generating data representing human heights.

**3. Exponentially Distributed Random Numbers**

- Used to represent the time between random events.
- Example: Time between two customers arriving at a bank.

**4. Poisson Distributed Random Numbers**

- Used to represent the number of events occurring within a fixed time or area.
- Example: Number of customers arriving at a bank in one minute.

### **4. How Are Distributed Random Numbers Used in Simulation?**

Consider a bank simulation:

1. Random numbers are generated according to a suitable distribution.
2. These numbers are used to represent customer arrival times.
3. Another set of random numbers represents customer service times.
4. The simulation uses these values to calculate waiting times and queue lengths.
5. The results help analyse the performance of the bank.

**Bank Simulation Flowchart 🏦**

**Generate Random Numbers**

**Apply Probability Distribution**

**Calculate Arrival and Service Times**

**Analyse Queue and Waiting Time**

### **5. Importance of Distributed Random Numbers**

1. **Realistic Simulation:** They help represent real-world randomness more accurately.
2. **Model Uncertainty:** They represent unpredictable events such as customer arrivals and machine failures.
3. **Better Analysis:** They help study different possible outcomes.
4. **Performance Testing:** They help test how a system behaves under different conditions.
5. **Decision Making:** They provide useful information for improving system performance.

### **6. Quick Revision 📝**

| Distribution | What it represents                   | Example                        |
| ------------ | ------------------------------------ | ------------------------------ |
| Uniform      | Equal chance of values               | Random number between 0 and 1  |
| Normal       | Values around an average             | Human height                   |
| Exponential  | Time between events                  | Time between customer arrivals |
| Poisson      | Number of events in a fixed interval | Customers arriving per minute  |

### **7. Important Exam Questions**

1. What are distributed random numbers? Explain with examples.
2. Explain different types of random numbers based on probability distributions.
3. Explain the importance of distributed random numbers in simulation.
4. How are distributed random numbers used in a banking simulation?

Remember this

**Random numbers + Probability Distribution = Distributed Random Numbers**

The selected distribution decides how frequently different values appear.

**Next topic:** Generation of Random Numbers.
