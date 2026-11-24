# Module III -- Introduction to Queuing Theory

## Important Exam Questions with Answers

**Subject:** Simulation and Modeling (IT71A)\
**Module:** III -- Introduction to Queuing Theory

Answers are written in simple, exam-ready English, followed by short
Hinglish summaries.

------------------------------------------------------------------------

## Q1. What is Queuing Theory? Explain its basic components and applications.

**Answer:** Queuing Theory is the mathematical study of waiting lines.
It is used to analyze situations in which entities arrive at a system,
wait for service if required, receive service and then leave.

A queuing system generally contains the following components:

1.  **Calling population:** The source from which customers or entities
    arrive. It may be finite or infinite.
2.  **Arrival process:** Describes how entities arrive, including the
    arrival rate and arrival pattern.
3.  **Waiting line (queue):** The place where entities wait when service
    is not immediately available.
4.  **Queue discipline:** The rule used to select the next entity for
    service, such as First Come First Served (FCFS).
5.  **Service mechanism:** Describes the number of servers, service
    channels and service phases.
6.  **Service time:** The time required to serve one entity.
7.  **System capacity:** The maximum number of entities allowed in the
    system, including those waiting and being served.

**Basic flow:**

``` text
Calling Population
        |
        v
     Arrivals
        |
        v
   Waiting Queue
        |
        v
      Service
        |
        v
      Exit
```

**Applications:** - Banks and ticket counters. - Hospitals and emergency
departments. - Computer networks and routers. - Operating systems and
CPU scheduling. - Manufacturing and production systems. - Customer
support centres.

**Hinglish:** Queuing Theory waiting lines ka study hai. Ismein
customers arrive karte hain, zarurat padne par queue mein wait karte
hain, service lete hain aur system se exit karte hain.

------------------------------------------------------------------------

## Q2. Explain the characteristics of a Queuing System.

**Answer:** The characteristics of a queuing system describe how
entities arrive, wait and receive service.

Important characteristics are:

1.  **Calling population:** The source of customers or entities. It may
    be finite or infinite.
2.  **Arrival process:** Describes the pattern and rate of arrivals.
    Arrivals may be deterministic or random.
3.  **Service mechanism:** Describes how service is provided, including
    the number of servers and service phases.
4.  **Number of channels:** The number of parallel servers available.
    For example, a bank may have three cashiers.
5.  **Number of phases:** The number of service stages an entity must
    pass through. For example, a patient may register and then consult a
    doctor.
6.  **Queue capacity:** The maximum number of entities that can wait or
    be present in the system, depending on the model definition.
7.  **Queue discipline:** The rule for selecting the next entity, such
    as FCFS, LCFS or priority.
8.  **Service time:** The time required to complete service for an
    entity.

**Hinglish:** Queuing system ki characteristics batati hain ki customers
kahan se aate hain, kitni speed se aate hain, kitne servers hain, kitni
der service hoti hai aur queue mein kis order se service milegi.

------------------------------------------------------------------------

## Q3. Explain Poisson's Formula and its applications.

**Answer:** The Poisson distribution is used to calculate the
probability of a given number of events occurring in a fixed time or
space interval when events occur independently at a constant average
rate.

The formula is:

\[ P(n)=`\frac{e^{-\lambda t}(\lambda t)^n}{n!}`{=tex} \]

Where: - (P(n)) = Probability of exactly (n) arrivals. -
(`\lambda`{=tex}) = Average arrival rate per unit time. - (t) = Time
interval. - (n) = Number of arrivals. - (e) = Mathematical constant
approximately equal to 2.718.

### Example

Suppose customers arrive at an average rate of 2 per minute. Find the
probability of exactly 3 arrivals in one minute.

Given:

\[ `\lambda=2`{=tex},`\quad `{=tex}t=1,`\quad `{=tex}n=3 \]

Substitute in the formula:

\[ P(3)=`\frac{e^{-2}(2\times1)^3}{3!}`{=tex} \]

\[ P(3)=`\frac{0.1353\times8}{6}`{=tex} \]

\[ P(3)`\approx0.1804`{=tex}=18.04% \]

Therefore, the probability of exactly 3 arrivals in one minute is
approximately 18.04%.

### Assumptions

-   Events occur independently.
-   The average event rate remains constant over the interval.
-   In a very small interval, the probability of more than one arrival
    is negligible.

### Applications

-   Customer arrivals at banks.
-   Calls arriving at call centres.
-   Packet arrivals in computer networks.
-   Patient arrivals at hospitals.

**Hinglish:** Poisson formula fixed time interval mein exactly n
arrivals hone ki probability calculate karta hai. Ismein average arrival
rate (`\lambda`{=tex}), time (t) aur arrivals ki sankhya (n) use hoti
hai.

------------------------------------------------------------------------

## Q4. Explain the Birth-Death Process in Queuing Theory.

**Answer:** A Birth-Death Process is a stochastic process in which the
state of a system changes through two types of events: births and
deaths.

-   **Birth:** An arrival that increases the number of entities in the
    system by one.
-   **Death:** A departure that decreases the number of entities in the
    system by one.

The state of the system is usually represented by the number of entities
present.

### Important terms

1.  **Birth rate ((`\lambda`{=tex})):** Average rate at which new
    entities arrive.
2.  **Death rate ((`\mu`{=tex})):** Average rate at which entities
    depart or complete service.
3.  **State:** Number of entities currently present in the system.

### Example

Consider a bank queue:

-   When a customer arrives, the number of customers increases by one.
    This is a birth.
-   When a customer completes service and leaves, the number decreases
    by one. This is a death.

``` text
State 0  <---->  State 1  <---->  State 2  <---->  State 3
          Birth/Death transitions between states
```

### Applications

-   Customer arrival and departure systems.
-   Telephone call systems.
-   Computer job processing.
-   Inventory systems.
-   Hospital patient flow.

**Hinglish:** Birth ka matlab arrival, jisse system mein entities ki
sankhya ek badhti hai. Death ka matlab departure, jisse entities ki
sankhya ek kam hoti hai.

------------------------------------------------------------------------

## Q5. Explain the Equilibrium of Queuing Systems.

**Answer:** Equilibrium in a queuing system refers to a steady-state
condition in which the probability of finding a certain number of
entities in the system becomes stable over time.

For a simple single-server queue, let:

-   (`\lambda`{=tex}) = Average arrival rate.
-   (`\mu`{=tex}) = Average service rate.

The stability condition is:

\[ `\lambda `{=tex}\< `\mu`{=tex} \]

This means the average service rate must be greater than the average
arrival rate.

### Conditions

1.  **Stable system ((`\lambda `{=tex}\< `\mu`{=tex})):** The server can
    handle arrivals on average, and a steady state may exist under the
    usual model assumptions.
2.  **Critical condition ((`\lambda `{=tex}= `\mu`{=tex})):** The system
    has no spare service capacity; a stable steady state does not exist
    for the standard infinite-capacity M/M/1 queue.
3.  **Unstable system ((`\lambda `{=tex}\> `\mu`{=tex})):** Arrivals
    exceed service capacity on average, so the queue tends to grow
    without bound in the standard model.

### Example

Suppose:

-   Arrival rate = 4 customers per hour.
-   Service rate = 6 customers per hour.

Since:

\[ 4 \< 6 \]

The system is stable under the standard single-server assumptions.

**Importance:** - Helps determine whether a queue can be maintained in
steady state. - Helps plan the required service capacity. - Helps avoid
continuously growing queues.

**Hinglish:** Equilibrium ka matlab system ka steady state.
Single-server queue stable tab hoti hai jab service rate (`\mu`{=tex}),
arrival rate (`\lambda`{=tex}) se zyada ho.

------------------------------------------------------------------------

## Q6. Explain different Queuing Disciplines.

**Answer:** Queuing Discipline is the rule used to decide which entity
will receive service next from a waiting queue.

Important types are:

### 1. First Come First Served (FCFS)

The entity that arrives first receives service first.

**Example:** People standing in a normal ticket queue.

### 2. Last Come First Served (LCFS)

The entity that arrives last receives service first.

**Example:** Items placed one above another in a stack, where the latest
item is removed first.

### 3. Service in Random Order (SIRO)

Entities are selected randomly for service, without considering their
arrival order.

**Example:** Selecting one waiting job randomly from a group.

### 4. Priority Queuing

Entities are served according to their assigned priority.
Higher-priority entities are served before lower-priority entities.

**Example:** Emergency patients are treated before non-emergency
patients.

Priority service can be:

-   **Preemptive:** A higher-priority entity can interrupt the service
    of a lower-priority entity.
-   **Non-preemptive:** The current service is completed before a
    higher-priority entity is served.

### Comparison

  Discipline   Service rule
  ------------ -------------------------------
  FCFS         First arrival served first
  LCFS         Latest arrival served first
  SIRO         Random selection
  Priority     Highest priority served first

**Hinglish:** Queuing discipline decide karti hai ki queue mein kis
customer ko pehle service milegi. FCFS mein jo pehle aaya, woh pehle
serve hoga; priority mein high-priority customer ko pehle service
milegi.

------------------------------------------------------------------------

## Q7. Explain the Simulation of a Single-Server Queue with an example.

**Answer:** A single-server queue is a queuing system in which entities
wait in a common queue and receive service from only one server.

Examples include a bank with one cashier or a single printer serving
multiple jobs.

### Steps

1.  Record the arrival time of each customer.
2.  Record the service time of each customer.
3.  Calculate the service start time.
4.  Calculate the service completion time.
5.  Calculate waiting time and time in the system.
6.  Calculate the server's idle time.

### Important formulas

\[ Service Start_i=`\max`{=tex}(Arrival_i,Service End\_{i-1}) \]

\[ Service End_i=Service Start_i+Service Time_i \]

\[ Waiting Time_i=Service Start_i-Arrival_i \]

\[ Time in System_i=Service End_i-Arrival_i \]

\[ Idle Time_i=`\max`{=tex}(0,Arrival_i-Service End\_{i-1}) \]

For the first customer, assume the previous service completion time is
0.

### Example

Consider four customers:

  Customer     Arrival time   Service time
  ---------- -------------- --------------
  C1                      0              3
  C2                      2              2
  C3                      3              3
  C4                      6              2

Simulation table:

  ---------------------------------------------------------------------------
  Customer        Arrival      Service  Service end Waiting time      Time in
                                 start                                 system
  ---------- ------------ ------------ ------------ ------------ ------------
  C1                    0            0            3            0            3

  C2                    2            3            5            1            3

  C3                    3            5            8            2            5

  C4                    6            8           10            2            4
  ---------------------------------------------------------------------------

Total waiting time:

\[ 0+1+2+2=5 \]

Average waiting time:

\[ `\frac{5}{4}`{=tex}=1.25`\text{ time units}`{=tex} \]

The server is busy from time 0 to 10, so total busy time is 10 time
units.

**Hinglish:** Single-server queue mein sirf ek server hota hai. Har
customer ka arrival aur service time use karke service start, service
end, waiting time aur idle time calculate karte hain.

------------------------------------------------------------------------

## Q8. Explain the Simulation of a Two-Server Queue with an example.

**Answer:** A two-server queue is a queuing system in which two servers
provide service to entities. In a common-queue arrangement, entities
wait in one queue and are assigned to whichever server becomes available
first.

### Steps

1.  Record the arrival time and service time of each entity.
2.  Maintain the next available time of both servers.
3.  When an entity arrives, assign it to the server that becomes
    available first.
4.  If both servers are busy, the entity waits.
5.  Calculate service start time, service end time and waiting time.
6.  Record busy time and idle time for both servers.

### Formulas

For customer (i), if the next available times of servers are (A_1) and
(A_2):

\[ Service Start_i=`\max`{=tex}(Arrival_i,`\min`{=tex}(A_1,A_2)) \]

Assign the customer to the server with the earlier available time, then
update that server's availability:

\[ New Available Time=Service Start_i+Service Time_i \]

\[ Waiting Time=Service Start-Arrival Time \]

### Example

Suppose the customer data is:

  Customer     Arrival time   Service time
  ---------- -------------- --------------
  C1                      0              3
  C2                      2              2
  C3                      3              3
  C4                      6              2

One possible schedule is:

  Customer   Server     Service start   Service end   Waiting time
  ---------- -------- --------------- ------------- --------------
  C1         S1                     0             3              0
  C2         S2                     2             4              0
  C3         S1                     3             6              0
  C4         S1                     6             8              0

During the interval from 0 to 8: - Server 1 busy time = 8 units. -
Server 2 busy time = 2 units. - Server 2 idle time = 6 units.

**Hinglish:** Two-server queue mein do servers hote hain. Common queue
se customer us server ko assign hota hai jo pehle free hota hai. Dono
busy hon toh customer wait karta hai.

------------------------------------------------------------------------

## Q9. Explain the M/M/1 Queuing Model and derive its important performance measures.

**Answer:** M/M/1 is a standard single-server queuing model.

The notation means:

-   First M: Markovian or Poisson arrival process.
-   Second M: Markovian or exponential service-time distribution.
-   1: One server.

### Assumptions

1.  Arrivals follow a Poisson process.
2.  Service times follow an exponential distribution.
3.  There is one server.
4.  Customers are served using FCFS discipline.
5.  The calling population and queue capacity are assumed infinite in
    the standard model.
6.  Arrival and service rates remain constant.
7.  Arrival and service processes are independent.
8.  The system is stable when (`\lambda `{=tex}\< `\mu`{=tex}).

### Important formulas

Let: - (`\lambda`{=tex}) = Arrival rate. - (`\mu`{=tex}) = Service
rate. - (`\rho`{=tex}) = Server utilization.

**1. Utilization:**

\[ `\rho`{=tex}=`\frac{\lambda}{\mu}`{=tex} \]

**2. Probability that the system is empty:**

\[ P_0=1-`\rho`{=tex} \]

**3. Average number of entities in the system:**

\[ L_s=`\frac{\lambda}{\mu-\lambda}`{=tex} \]

**4. Average number of entities waiting in the queue:**

\[ L_q=`\frac{\lambda^2}{\mu(\mu-\lambda)}`{=tex} \]

**5. Average time spent in the system:**

\[ W_s=`\frac{1}{\mu-\lambda}`{=tex} \]

**6. Average waiting time in the queue:**

\[ W_q=`\frac{\lambda}{\mu(\mu-\lambda)}`{=tex} \]

### Numerical Example

Suppose:

-   Arrival rate (`\lambda=4`{=tex}) customers/hour.
-   Service rate (`\mu=6`{=tex}) customers/hour.

**Utilization:**

\[ `\rho`{=tex}=`\frac{4}{6}`{=tex}=0.667=66.7% \]

**Probability of an empty system:**

\[ P_0=1-0.667=0.333 \]

**Average number in the system:**

\[ L_s=`\frac{4}{6-4}`{=tex}=2 \]

**Average number in the queue:**

\[ L_q=`\frac{4^2}{6(6-4)}`{=tex}=`\frac{16}{12}`{=tex}=1.33 \]

**Average time in the system:**

\[
W_s=`\frac{1}{6-4}`{=tex}=0.5`\text{ hour}`{=tex}=30`\text{ minutes}`{=tex}
\]

**Average waiting time in the queue:**

\[
W_q=`\frac{4}{6(6-4)}`{=tex}=`\frac{4}{12}`{=tex}=0.333`\text{ hour}`{=tex}=20`\text{ minutes}`{=tex}
\]

### Little's Law

Little's Law relates average number of entities to arrival rate and
average time:

\[ L_s=`\lambda `{=tex}W_s \]

\[ L_q=`\lambda `{=tex}W_q \]

**Hinglish:** M/M/1 ek single-server queue model hai. Pehla M Poisson
arrivals, doosra M exponential service time aur 1 ka matlab ek server.
Is model se utilization, average queue length aur waiting time calculate
kar sakte hain.

------------------------------------------------------------------------

## Q10. Explain the applications of Queuing Theory in Operating Systems and Computer Networks.

**Answer:** Queuing Theory is widely used in computer systems to study
waiting lines, processing delays, resource usage and system performance.

### A. Applications in Operating Systems

1.  **CPU scheduling:** Processes wait in the ready queue until the CPU
    becomes available.
2.  **Disk scheduling:** Disk requests wait in a queue before being
    processed.
3.  **Process management:** Operating systems manage processes waiting
    for different resources.
4.  **Memory management:** Requests for memory resources may wait when
    availability is limited.
5.  **Printer management:** Print jobs wait in a queue until the printer
    is available.

### B. Applications in Computer Networks

1.  **Router and switch queues:** Incoming packets wait in buffers
    before transmission.
2.  **Packet transmission:** Queuing models help analyze packet
    processing and transmission delays.
3.  **Network congestion:** Long queues indicate congestion and possible
    packet loss.
4.  **Quality of Service (QoS):** Priority queues help serve important
    traffic before less critical traffic.
5.  **Server request handling:** Web and application servers manage
    incoming requests through queues.

### Advantages

-   Helps estimate waiting and response times.
-   Identifies bottlenecks.
-   Helps improve resource utilization.
-   Supports capacity planning.
-   Helps reduce congestion and delays.

**Hinglish:** Operating System mein CPU, disk aur printer ke jobs queues
mein wait karte hain. Networks mein packets router aur switch ke buffers
mein wait karte hain. Queuing Theory waiting time, congestion aur
resource utilization analyze karne mein help karti hai.

------------------------------------------------------------------------

# Quick Formula Revision

  -----------------------------------------------------------------------------------------------------------
  Concept                             Formula
  ----------------------------------- -----------------------------------------------------------------------
  Poisson probability                 (P(n)=`\frac{e^{-\lambda t}(\lambda t)^n}{n!}`{=tex})

  Stability condition for M/M/1       (`\lambda`{=tex}\<`\mu`{=tex})

  M/M/1 utilization                   (`\rho`{=tex}=`\lambda`{=tex}/`\mu`{=tex})

  Empty-system probability            (P_0=1-`\rho`{=tex})

  Average number in system            (L_s=`\lambda`{=tex}/(`\mu`{=tex}-`\lambda`{=tex}))

  Average queue length                (L_q=`\lambda`{=tex}\^2/\[`\mu`{=tex}(`\mu`{=tex}-`\lambda`{=tex})\])

  Average time in system              (W_s=1/(`\mu`{=tex}-`\lambda`{=tex}))

  Average queue waiting time          (W_q=`\lambda`{=tex}/\[`\mu`{=tex}(`\mu`{=tex}-`\lambda`{=tex})\])

  Little's Law                        (L_s=`\lambda `{=tex}W_s, L_q=`\lambda `{=tex}W_q)

  Single-server service start         (`\max`{=tex}(Arrival, Previous Service End))

  Waiting time                        Service start − Arrival

  Time in system                      Service end − Arrival
  -----------------------------------------------------------------------------------------------------------

# Last-Minute Preparation Tips

1.  Prepare Q1 and Q2 to understand the basic structure and
    characteristics of queuing systems.
2.  Practice the Poisson formula numerical question.
3.  Learn the Birth-Death Process and equilibrium condition
    (`\lambda `{=tex}\< `\mu`{=tex}).
4.  Memorize FCFS, LCFS, SIRO and Priority disciplines.
5.  Practice the single-server and two-server simulation tables.
6.  Memorize the M/M/1 assumptions and formulas; practice at least one
    numerical problem.
7.  Prepare the applications of queuing theory in Operating Systems and
    Computer Networks.

**End of Module III -- Important Questions and Answers.**
