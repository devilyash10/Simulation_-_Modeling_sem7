# **Module V – Program Control Statements in GPSS**

Important exam topic

This is an important topic because program control statements determine how a GPSS simulation starts, runs, controls transactions and stops.

We'll cover the meaning, important statements, examples, working and exam points in simple English.

## **1. Introduction**

**Program Control Statements** are instructions used to control the execution of a GPSS simulation program.

They help define how the simulation starts, how long it runs, how transactions are generated and when the simulation stops.

In simple words, they control the overall execution of the simulation.

## **2. Important Program Control Statements**

The following statements and commands are commonly used in GPSS-based simulation programs.

## **2. Main Program Control Statements**

For your exam, remember these **five important statements**:

1. SIMULATE
2. RESET
3. CLEAR
4. JOB
5. END

Also remember **START**, which is used to initiate a simulation run.

### **1. SIMULATE Statement**

- SIMULATE is used to indicate that the GPSS simulation program is to be executed.
- It is generally written at the beginning of a GPSS program.
- It prepares the model for simulation.

**Example:**

```
SIMULATE
```

**Hinglish:** Ye GPSS ko batata hai ki simulation model execute karna hai.

### **2. RESET Statement**

- RESET clears the statistics collected during the previous simulation run.
- It does not remove the existing transactions from the model.
- It is useful when we want to collect statistics again without starting the entire model from the beginning.

**Example:**

```
RESET
```

**Hinglish:** RESET sirf statistics ko zero karta hai, lekin existing transactions ko remove nahi karta.

### **3. CLEAR Statement**

- CLEAR removes all transactions from the model.
- It also resets the statistics collected during the previous run.
- It allows the simulation to start again from the beginning.
- In classic GPSS, it does not reset the random-number generator seeds.

**Example:**

```
CLEAR
```

**Hinglish:** CLEAR statistics bhi clear karta hai aur saare transactions bhi remove kar deta hai. Simulation fresh start hoti hai.

### **4. JOB Statement**

- JOB is used to end the current simulation model and start a new problem.
- It removes the model information preceding the JOB statement.
- It resets the random-number generator seeds in the classic GPSS context.

**Example:**

```
JOB
```

**Hinglish:** JOB ka use ek simulation problem ko close karke next new problem start karne ke liye hota hai.

### **5. START Statement**

- START is used to begin the execution of a simulation.
- Its operand specifies the initial value of the termination counter.
- The simulation stops when transactions entering TERMINATE reduce this counter to zero.

**Example:**

```
START 100
```

Here, the simulation starts with a termination count of 100. If each completed transaction enters `TERMINATE 1`, the run stops after 100 such completions.

**Hinglish:** START simulation ko run karta hai. Isme diya gaya number batata hai ki termination counter ki initial value kya hogi.

### **6. END Statement**

- END indicates the end of a GPSS program.
- It is written at the end of the program.
- It marks the completion of the simulation program.

**Example:**

```
END
```

**Hinglish:** END program ki last statement hoti hai, jo batati hai ki GPSS code yahan khatam hota hai.

## **3. Difference Between RESET, CLEAR and JOB**

This is a very important comparison for exams.

| Basis        | RESET                    | CLEAR                              | JOB                               |
| ------------ | ------------------------ | ---------------------------------- | --------------------------------- |
| Purpose      | Clears statistics        | Clears statistics and transactions | Starts a new problem              |
| Transactions | Remain in model          | Removed                            | Previous model removed            |
| Statistics   | Reset                    | Reset                              | Previous model statistics removed |
| Random seeds | Not reset                | Not reset                          | Reset in classic GPSS             |
| Use          | Collect fresh statistics | Restart same model                 | Start another model               |

**Hinglish trick to remember:**

- RESET = Only statistics clear.
- CLEAR = Statistics + Transactions clear.
- JOB = Previous model remove, new problem start.

These distinctions follow the classic GPSS control-statement description.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.vssut.ac.in\&sz=32)

P a g e+2



## **4. Example of GPSS Program Control Statements**

```
SIMULATE

GENERATE 5
ADVANCE 3
TERMINATE 1

START 100
END
```

**Explanation:**

1. `SIMULATE` – Indicates the simulation program.
2. `GENERATE 5` – Generates transactions at intervals of 5 time units.
3. `ADVANCE 3` – Delays each transaction by 3 time units.
4. `TERMINATE 1` – Removes a transaction and reduces the termination counter by 1.
5. `START 100` – Starts simulation with a termination count of 100.
6. `END` – Marks the end of the program.

## **5. Importance of Program Control Statements**

1. **Execution Control:** Controls the execution of the simulation program.
2. **Statistics Management:** Helps reset and clear collected statistics.
3. **Simulation Restart:** Allows the same model to be executed again.
4. **Multiple Experiments:** Helps perform different simulation experiments.
5. **Program Completion:** Defines when the program starts and ends.

## **6. Quick Revision Table**

| Statement | Main function                      |
| --------- | ---------------------------------- |
| SIMULATE  | Indicates simulation execution     |
| RESET     | Clears statistics                  |
| CLEAR     | Clears statistics and transactions |
| JOB       | Starts a new problem               |
| START     | Starts simulation                  |
| END       | Ends the program                   |

## **7. Important Exam Questions**

1. What are Program Control Statements in GPSS? Explain their types.
2. Explain SIMULATE, RESET and CLEAR statements.
3. Differentiate between RESET, CLEAR and JOB.
4. Explain START and END statements with examples.
5. Write a short note on GPSS Program Control Statements.

Exam preparation priority

**My suggestion:** Prepare Q1, Q3 and Q4 thoroughly. Together, they cover almost all the important statements.

**Next topic: SIMSCRIPT – Organization and Program.**