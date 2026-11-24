# Module IV -- Discrete-Event Simulation

## Important Exam Questions with Answers

**Subject:** Simulation and Modeling (IT71A)\
**Module:** IV -- Discrete-Event Simulation

Answers are written in simple, exam-ready English, followed by short
Hinglish summaries.

------------------------------------------------------------------------

## Q1. What is Discrete-Event Simulation? Explain its characteristics and applications.

**Answer:** Discrete-Event Simulation (DES) is a simulation technique in
which the state of a system changes only at specific points in time
called events. Events are processed in chronological order using a
simulation clock.

**Example:** In a bank, customer arrival, service start and customer
departure are events. Each event may change the system state.

**Characteristics:** 1. Event-based: the system changes when an event
occurs. 2. Simulation clock: maintains the current simulated time. 3.
Event scheduling: events are arranged according to occurrence time. 4.
State changes: events may change the system condition. 5. Time
advancement: the clock moves from one event to the next. 6. Statistics
collection: waiting time, queue length and utilization are recorded.

**Applications:** Banking, computer networks, operating systems,
manufacturing and hospitals.

**Hinglish:** DES mein system ki state sirf tab change hoti hai jab koi
event occur hota hai, jaise customer arrival, service start ya
departure.

------------------------------------------------------------------------

## Q2. Explain the main components of a Simulation Model with examples.

**Answer:** A simulation model represents the working of a real-world
system. Its main components are:

1.  **Entities:** Objects that move through or interact with a system.
    Example: customers or network packets.
2.  **Attributes:** Properties of an entity. Example: customer ID,
    arrival time and service time.
3.  **Variables:** Values representing the overall system condition.
    Example: number of customers waiting.
4.  **Resources:** Facilities required to perform activities. Example:
    cashiers or machines.
5.  **Events:** Occurrences that change the system state. Example:
    customer arrival or service completion.
6.  **Activities:** Operations performed over a period of time. Example:
    serving a customer.
7.  **Simulation clock:** Represents current simulated time and advances
    from one event time to the next.
8.  **Statistical counters:** Collect performance information. Example:
    average waiting time and resource utilization.

**Bank example:**

  Component             Example
  --------------------- -------------------------------
  Entity                Customer
  Attribute             Customer ID, arrival time
  Variable              Number of customers waiting
  Resource              Cashier
  Event                 Customer arrival or departure
  Activity              Customer service
  Simulation clock      Current simulated time
  Statistical counter   Average waiting time

**Hinglish:** Entity object hai, attribute uski property, variable
system ki changing information, resource kaam ki facility, event state
change karta hai aur activity time leti hai.

------------------------------------------------------------------------

## Q3. Explain the organization of a Simulation Model with a flowchart.

**Answer:** Organization of a simulation model refers to the way
different parts of a simulation program are arranged to represent a
real-world system.

**Main steps:** 1. **Initialization:** Set initial values of variables,
clock, resources and counters. 2. **Input data:** Provide arrival times,
service times and other required information. 3. **Event scheduling:**
Arrange events according to their scheduled time. 4. **Event
processing:** Execute the selected event and update the system state. 5.
**Time advancement:** Move the clock to the next scheduled event. 6.
**Statistics collection:** Record waiting time, queue length and
utilization. 7. **Termination:** Stop when the specified condition is
satisfied and display results.

**Flowchart:**

``` text
        Initialization
              |
        Read Input Data
              |
       Schedule Next Event
              |
      Advance Simulation Clock
              |
       Process Event and
        Update the System
              |
       Collect Statistics
              |
      Termination Condition?
          /          \
        No            Yes
        |              |
  Schedule Next    Display Results
      Event              |
        |                v
        +------------> Stop
```

**Hinglish:** Model ko proper order mein organize karte hain:
initialization, input, event scheduling, event processing, time advance,
statistics collection aur termination.

------------------------------------------------------------------------

## Q4. What are events and variables in Discrete-Event Simulation? Explain their types with examples.

**Answer:** Events are occurrences that cause a change in the state of a
system. Variables represent and track the current condition or
information of the system.

### Events

1.  **Arrival event:** A new entity enters the system. Example: customer
    enters a bank.
2.  **Departure event:** An entity leaves the system. Example: customer
    leaves after service.
3.  **Service completion event:** Processing is completed. Example:
    cashier finishes serving a customer.
4.  **Resource failure event:** A resource stops working. Example:
    machine breakdown.
5.  **Resource repair event:** A failed resource becomes operational
    again.

### Variables

1.  **State variables:** Describe the current system condition. Example:
    number of customers in a queue.
2.  **Counter variables:** Count occurrences or completed activities.
    Example: total customers served.
3.  **Time variables:** Store time-related information. Example: current
    simulation time and arrival time.

  Events                              Variables
  ----------------------------------- ---------------------------------------
  Represent occurrences.              Represent system information.
  Cause changes in system state.      Store system state or other values.
  Occur at specific points in time.   May change during simulation.
  Example: Customer arrival.          Example: Number of customers waiting.

**Hinglish:** Event ka matlab hai "kya hua?" aur variable ka matlab hai
"system ki current condition kya hai?"

------------------------------------------------------------------------

## Q5. Explain the different approaches for Time Advance in Discrete-Event Simulation.

**Answer:** Time Advance is the process of moving the simulation clock
forward. There are two main approaches.

### 1. Fixed Time Increment Approach

Also called the **Time-Driven Approach**. - Simulation time advances by
a fixed interval. - The system is checked at every interval to identify
whether an event has occurred. - Example: clock advances as 0, 1, 2, 3,
4 and 5 minutes.

**Advantages:** Simple to implement; useful for regular time-based
changes.\
**Disadvantages:** May perform unnecessary checks; small intervals
require more computation; large intervals may miss important timing
details.

### 2. Next Event Time Advance Approach

Also called the **Event-Driven Approach**. - The clock advances directly
to the time of the next scheduled event. - Only scheduled events are
processed. - Example: if events are at times 2, 5 and 9, the clock moves
0 → 2 → 5 → 9.

**Advantages:** Avoids unnecessary checks; efficient for irregular
events.\
**Disadvantages:** Requires an event list; scheduling can be complex;
simultaneous events need proper handling.

  Fixed Time Increment              Next Event Time Advance
  --------------------------------- ----------------------------------
  Advances by fixed intervals.      Advances to the next event.
  Checks at every interval.         Processes scheduled events only.
  May perform unnecessary checks.   Avoids unnecessary checks.
  Easier to implement.              Requires event scheduling.
  Time-driven.                      Event-driven.

**Hinglish:** Fixed approach mein clock fixed interval par badhta hai.
Next-event approach mein clock directly next event ke time par jump
karta hai.

------------------------------------------------------------------------

## Q6. Explain the Generation of Arrival Patterns and their types.

**Answer:** Generation of Arrival Patterns is the process of determining
how entities enter a system during simulation. An arrival pattern
describes when entities arrive, how frequently they arrive and the time
between consecutive arrivals.

### Types

1.  **Deterministic arrival pattern:** Entities arrive at fixed
    intervals. Example: a bus arrives every 10 minutes.
2.  **Random or stochastic arrival pattern:** Entities arrive at
    irregular and unpredictable intervals. Example: customers arriving
    at a shopping mall.
3.  **Poisson arrival pattern:** A commonly used random arrival model in
    which arrivals occur independently at a constant average rate.
    Inter-arrival times follow an exponential distribution.

**Poisson probability formula:**

\[ P(n)=`\frac{e^{-\lambda t}(\lambda t)^n}{n!}`{=tex} \]

Where (P(n)) is probability of n arrivals, (`\lambda`{=tex}) is average
arrival rate, (t) is time interval and (n) is number of arrivals.

**Exponential inter-arrival time:**

\[ T=-`\frac{\ln(U)}{\lambda}`{=tex} \]

Where (T) is inter-arrival time, (U) is a uniform random number between
0 and 1, and (`\lambda`{=tex}) is average arrival rate.

**Example:** If (U=0.5) and (`\lambda=2`{=tex}) arrivals per minute:

\[ T=-`\frac{\ln(0.5)}{2}`{=tex}=0.3466`\text{ minutes}`{=tex} \]

Methods include fixed interval method, probability distribution method,
random number method and historical data method.

**Applications:** Banking, hospitals, computer networks, manufacturing
and airports.

**Hinglish:** Arrival pattern batata hai entities system mein kab aur
kitne interval par enter karengi. Deterministic mein fixed interval hota
hai, random mein interval badalta hai aur Poisson model average constant
arrival rate ke saath random arrivals represent karta hai.

------------------------------------------------------------------------

## Q7. Explain the important Simulation Programming Tasks.

**Answer:** Simulation Programming Tasks are activities performed while
developing and executing a simulation program.

1.  **Defining the system:** Understand the real-world system and its
    operations.
2.  **Defining entities and variables:** Identify objects, attributes
    and variables.
3.  **Generating random numbers:** Represent uncertain activities such
    as arrival and service times.
4.  **Scheduling events:** Arrange events according to occurrence time.
5.  **Advancing simulation time:** Move the clock to the next scheduled
    event.
6.  **Processing events:** Execute events and update the system state.
7.  **Collecting statistics:** Record waiting time, queue length and
    utilization.
8.  **Displaying and analyzing results:** Display final results and
    evaluate system performance.

**Example:** In a bank simulation, define customers and cashiers,
generate arrival times, schedule service events, update the queue and
calculate average waiting time.

**Hinglish:** Ismein system define karna, entities aur variables
identify karna, random numbers generate karna, events schedule/process
karna, statistics collect karna aur results analyze karna shamil hai.

------------------------------------------------------------------------

## Q8. What is Gathering Statistics in Simulation? Explain important performance measures.

**Answer:** Gathering Statistics is the process of collecting and
recording information during simulation to measure system performance.

1.  **Waiting time:** Time an entity waits before receiving service.

\[ Waiting Time=Service Start Time-Arrival Time \]

2.  **Service time:** Time required to complete service.

\[ Service Time=Service End Time-Service Start Time \]

3.  **Queue length:** Number of entities waiting for service at a
    particular time.
4.  **Average waiting time:**

\[
Average Waiting Time=`\frac{Total\ Waiting\ Time}{Total\ Customers}`{=tex}
\]

5.  **Resource utilization:** Percentage of available time a resource
    remains busy.

\[
Utilization=`\frac{Busy\ Time}{Total\ Available\ Time}`{=tex}`\times100`{=tex}
\]

6.  **Throughput:** Total number of entities processed during a given
    period.
7.  **Idle time:** Period during which a resource remains unused.

\[ Idle Time=Total Available Time-Busy Time \]

**Methods:** Counters count events; accumulators calculate totals;
time-based recording measures duration in a state; frequency
distributions record how often values occur; average calculations find
mean performance.

**Hinglish:** Statistics collect karke average waiting time, queue
length, throughput, utilization aur idle time calculate karte hain. Isse
system ki efficiency pata chalti hai.

------------------------------------------------------------------------

## Q9. Explain Occupancy and Utilization. Differentiate between them.

**Answer:** Occupancy and Utilization are performance measures used to
evaluate how effectively system capacity and resources are being used.

### Occupancy

Occupancy refers to the number of entities or the amount of system
capacity occupied at a particular time.

Example: If a bank has capacity for 20 customers and 12 are present,
occupancy is 12 customers.

Average occupancy:

\[
Average Occupancy=`\frac{Area\ under\ occupancy-time\ curve}{Total\ Simulation\ Time}`{=tex}
\]

### Utilization

Utilization measures the percentage of time a resource remains busy
compared to its total available time.

\[
Utilization=`\frac{Busy\ Time}{Total\ Available\ Time}`{=tex}`\times100`{=tex}
\]

Example: If a cashier is busy for 40 minutes during a 60-minute
simulation:

\[ Utilization=`\frac{40}{60}`{=tex}`\times100`{=tex}=66.67% \]

  -----------------------------------------------------------------------
  Occupancy                           Utilization
  ----------------------------------- -----------------------------------
  Measures number of entities or      Measures how much a resource is
  capacity occupied.                  used over time.

  Indicates system load.              Indicates resource usage
                                      efficiency.

  Measured in entities or percentage  Usually expressed as percentage of
  of capacity.                        available time.

  Example: 12 customers in a bank.    Example: Cashier busy 66.67% of the
                                      time.
  -----------------------------------------------------------------------

**Hinglish:** Occupancy batata hai kitne customers ya kitni capacity
occupied hai. Utilization batata hai resource available time mein kitne
percent busy raha.

------------------------------------------------------------------------

## Q10. Explain Recording Distributions and its methods.

**Answer:** Recording Distributions is the process of collecting and
recording the frequency of different values obtained during a
simulation.

### Methods

1.  **Frequency distribution:** Records how many times a value or range
    occurs.

  Waiting time (minutes)     Number of customers
  ------------------------ ---------------------
  0--2                                         5
  2--4                                        10
  4--6                                         8
  6--8                                         2

2.  **Histogram:** A graphical representation of a frequency
    distribution using bars.
3.  **Cumulative frequency distribution:** Records the running total of
    frequencies.

  Waiting time (minutes)     Frequency   Cumulative frequency
  ------------------------ ----------- ----------------------
  0--2                               5                      5
  2--4                              10                     15
  4--6                               8                     23
  6--8                               2                     25

Here, 23 customers waited less than 6 minutes.

**Purpose:** Understand system behaviour, analyze waiting and service
times, identify common outcomes and compare simulation results.

**Hinglish:** Recording Distributions mein results ko frequency ke
according record karte hain. Frequency table, histogram aur cumulative
frequency se pata chalta hai ki values kitni baar occur hui hain.

------------------------------------------------------------------------

## Q11. What are Transit Times? Explain their calculation and importance.

**Answer:** Transit Time is the total time taken by an entity to move
through a system, from its entry point to its exit point.

\[ Transit Time=Exit Time-Entry Time \]

For a simple queuing system:

\[ Transit Time=Waiting Time+Service Time \]

**Example:** A customer enters a bank at 10:00 AM, service starts at
10:05 AM and ends at 10:10 AM. - Waiting time = 5 minutes. - Service
time = 5 minutes. - Transit time = 10 minutes.

Average transit time:

\[
Average Transit Time=`\frac{Total\ Transit\ Time}{Total\ Number\ of\ Entities}`{=tex}
\]

If three customers have transit times of 10, 15 and 20 minutes:

\[ Average=`\frac{10+15+20}{3}`{=tex}=15`\text{ minutes}`{=tex} \]

**Applications:** Banking, computer networks, manufacturing, hospitals
and transportation.

**Importance:** Measures system efficiency, identifies delays, improves
service quality and supports resource planning.

**Hinglish:** Transit Time entity ke system mein enter hone se lekar
exit hone tak ka total time hai. Simple queue mein Transit Time =
Waiting Time + Service Time.

------------------------------------------------------------------------

# Quick Formula Revision

  -------------------------------------------------------------------------------------------
  Concept                             Formula
  ----------------------------------- -------------------------------------------------------
  Poisson probability                 (P(n)=`\frac{e^{-\lambda t}(\lambda t)^n}{n!}`{=tex})

  Exponential inter-arrival time      (T=-`\frac{\ln(U)}{\lambda}`{=tex})

  Waiting time                        Service start − Arrival time

  Service time                        Service end − Service start

  Average waiting time                Total waiting time ÷ Number of customers

  Utilization                         (Busy time ÷ Available time) × 100

  Idle time                           Available time − Busy time

  Average occupancy                   Area under occupancy-time curve ÷ Total time

  Transit time                        Exit time − Entry time

  Average transit time                Total transit time ÷ Number of entities
  -------------------------------------------------------------------------------------------

# Last-Minute Preparation Tips

1.  Prepare Q1, Q2 and Q3 thoroughly: they cover the basics and
    structure of discrete-event simulation.
2.  Learn the difference between fixed time increment and next-event
    time advance.
3.  Practice the Poisson and exponential inter-arrival time formulas.
4.  Memorize formulas for waiting time, utilization, idle time and
    transit time.
5.  Prepare the difference between occupancy and utilization.
6.  Practice the flowchart for organization of a simulation model.

**End of Module IV -- Important Questions and Answers.**
