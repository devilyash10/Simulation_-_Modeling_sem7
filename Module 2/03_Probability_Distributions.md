# **Module II – Probability Concepts in Simulation**

## **Topic 3: Probability Distributions**

### **1. What is a Probability Distribution?**

A **probability distribution** is a mathematical way of showing all the possible values of a random variable and the probability of getting each value.

In simple words, it tells us **what outcomes are possible and how likely each outcome is to happen.**

### **2. Simple Example 🎲**

Suppose we roll a fair dice.

The possible outcomes are 1, 2, 3, 4, 5 and 6. Each outcome has an equal probability of \\(1/6\\).

| Dice outcome | Probability |
| ------------ | ----------- |
| 1            | 1/6         |
| 2            | 1/6         |
| 3            | 1/6         |
| 4            | 1/6         |
| 5            | 1/6         |
| 6            | 1/6         |

This table is called a probability distribution because it shows all possible outcomes and their probabilities.

The sum of all probabilities is always 1.

\\[ \sum P(X=x)=1 \\]

### **3. Types of Probability Distributions**

Probability distributions are mainly divided into two types:

**Probability Distributions**

**Discrete**

Countable values

Examples:

• Binomial

• Poisson

**Continuous**

Values in a range

Examples:

• Normal

• Uniform

• Exponential

### **A. Discrete Probability Distribution**

**Definition:** A discrete probability distribution describes the probabilities of all possible countable values of a random variable.

**Example:** Number of customers arriving at a bank in one hour.

It may be 0, 1, 2, 3, 4 or more customers.

**Common discrete distributions:**

1\. **Binomial Distribution:** Used when we count the number of successes in a fixed number of trials.

Example: Number of students passing an exam out of 10 students.

2\. **Poisson Distribution:** Used to calculate the probability of a certain number of events occurring in a fixed time or space.

Example: Number of customers arriving at a bank in one minute.

### **B. Continuous Probability Distribution**

**Definition:** A continuous probability distribution describes the probabilities of a random variable that can take any value within a given range.

**Example:** Time taken by a customer to complete a banking transaction.

It may be 2 minutes, 2.5 minutes, 2.75 minutes, etc.

**Common continuous distributions:**

1\. **Normal Distribution:** Used for data that is distributed around an average value, forming a bell-shaped curve.

Example: Heights of people in a large population (approximately).

2\. **Uniform Distribution:** Used when all values within a given range are equally likely.

Example: A random number generated between 0 and 1.

3\. **Exponential Distribution:** Commonly used to represent the time between two consecutive random events.

Example: Time between customer arrivals at a bank when arrivals follow a Poisson process.

### **4. Difference Between Discrete and Continuous Probability Distributions**

| Discrete Distribution                         | Continuous Distribution                     |
| --------------------------------------------- | ------------------------------------------- |
| Deals with countable values.                  | Deals with values within a range.           |
| Uses a Probability Mass Function (PMF).       | Uses a Probability Density Function (PDF).  |
| Probability is assigned to individual values. | Probability is calculated over an interval. |
| Sum of probabilities is 1.                    | Total area under the curve is 1.            |
| Examples: Binomial and Poisson.               | Examples: Normal and Exponential.           |

### **5. Importance of Probability Distributions in Simulation**

- **Represent randomness:** They help represent random events in real-world systems.
- **Generate random values:** They help generate values for simulation experiments.
- **Predict outcomes:** They help estimate the chances of different outcomes.
- **Model real systems:** They are used in banking, traffic, manufacturing and computer networks.
- **Improve decisions:** They help analyse uncertain situations before making decisions.

### **6. Quick Revision 📝**

| Distribution | Easy meaning                         | Example               |
| ------------ | ------------------------------------ | --------------------- |
| Binomial     | Number of successes in fixed trials  | Students passing      |
| Poisson      | Number of events in a fixed interval | Customer arrivals     |
| Normal       | Values around an average             | Human height          |
| Uniform      | All values in a range equally likely | Random number         |
| Exponential  | Waiting time between events          | Time between arrivals |

### **7. Important Exam Questions**

1. Define probability distribution and explain its types.
2. Explain discrete and continuous probability distributions with examples.
3. Write short notes on Binomial, Poisson, Normal, Uniform and Exponential distributions.
4. Explain the importance of probability distributions in simulation.

Exam preparation tip

For a 10–14 marks question, prepare the definition, two main types, examples of common distributions, a comparison table and applications.

**Remember:** Probability distribution = Possible values + Their probabilities.

**Next topic:** Distributed Random Numbers.