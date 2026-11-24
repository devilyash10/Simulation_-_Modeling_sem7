# Module V -- Simulation Languages

## Important Exam Questions and Answers \| B.Tech IT -- RGPV

**How to use these notes:** Answers are written in simple English with
definitions, key points, examples, and short Hinglish explanations. They
are designed as revision material for long-answer questions. GPSS and
SIMSCRIPT syntax can differ between versions, so examples are simplified
and should be matched with the notation taught in class.

------------------------------------------------------------------------

## Q1. What are simulation languages? Explain their need and advantages.

### Answer

A **simulation language** is a programming language or software tool
used to create, run, and study a model of a real-world system. It
provides features that make it easier to represent system components,
events, resources, queues, and the passage of simulation time.

Examples include **GPSS (General Purpose Simulation System)** and
**SIMSCRIPT**.

### Need for simulation languages

1.  **Easy model development:** They provide ready-made commands for
    common simulation activities.
2.  **Event handling:** They help schedule and process events in the
    correct time order.
3.  **Resource management:** They can represent resources such as
    machines, counters, processors, and service staff.
4.  **Queue handling:** They support waiting lines and help collect
    waiting-time statistics.
5.  **Time management:** They provide ways to advance the simulation
    clock.
6.  **Statistical analysis:** They can collect information such as
    average waiting time, utilization, and queue length.

### Advantages

-   Reduce the amount of code required to build a simulation.
-   Make complex systems easier to represent.
-   Provide facilities for collecting statistics.
-   Help test different operating conditions without disturbing the real
    system.
-   Make it easier to repeat experiments with different input values.

**Example:** A bank can be modeled to study customer arrivals, waiting
lines, and the workload of service counters before changing the actual
counter arrangement.

**Hinglish summary:** Simulation language ek special programming tool
hai jo real system ka model banane, events chalane aur statistics
collect karne mein help karta hai. GPSS aur SIMSCRIPT iske examples
hain.

------------------------------------------------------------------------

## Q2. Explain GPSS and its basic concepts.

### Answer

**GPSS (General Purpose Simulation System)** is a simulation language
mainly used for **discrete-event simulation**. It represents a system as
a sequence of blocks through which transactions move.

GPSS is often called a **transaction-oriented** or **block-oriented**
simulation language.

### Basic concepts of GPSS

1.  **Transaction:** A transaction represents an entity moving through
    the model. It may represent a customer, job, telephone call, or
    product.
2.  **Block:** A block is a predefined instruction that performs an
    operation, such as generating a transaction, making it wait, or
    occupying a resource.
3.  **Facility:** A facility represents a single-capacity resource, such
    as one bank counter or one CPU.
4.  **Storage:** Storage represents a resource that can serve multiple
    transactions at the same time, up to its capacity.
5.  **Queue:** A queue represents a waiting line formed when
    transactions cannot immediately obtain a required resource.
6.  **Simulation clock:** It represents the current simulated time.
7.  **Event:** An event is an occurrence that changes the state of the
    system, such as an arrival or service completion.

### Common GPSS blocks

  Block         Purpose
  ------------- -------------------------------------------
  `GENERATE`    Creates transactions
  `QUEUE`       Records entry into a waiting line
  `SEIZE`       Captures a facility
  `DEPART`      Records departure from a queue
  `ADVANCE`     Delays a transaction for a specified time
  `RELEASE`     Frees a facility
  `TERMINATE`   Removes a transaction from the simulation

### Example: Bank counter

A customer arrives, waits if the counter is busy, occupies the counter,
receives service, and then leaves.

``` text
GENERATE 5
QUEUE LINE
SEIZE COUNTER
DEPART LINE
ADVANCE 3
RELEASE COUNTER
TERMINATE 1
```

This is a simplified illustration of the flow. The `GENERATE` block
creates customers at the specified interval, while `ADVANCE` represents
service time.

**Hinglish summary:** GPSS mein customer ya job ko transaction kehte
hain. Transaction predefined blocks se pass hota hai. Facility single
resource hota hai, jaise bank counter, aur queue waiting line hoti hai.

------------------------------------------------------------------------

## Q3. Explain the important blocks used in GPSS.

### Answer

GPSS uses predefined blocks to describe the movement and activities of
transactions in a system.

1.  **GENERATE:** Creates new transactions at specified time intervals.
    In a bank model, it can generate arriving customers.
2.  **QUEUE:** Records a transaction entering a waiting line. It is
    useful for calculating queue statistics.
3.  **SEIZE:** Attempts to capture a facility. If the facility is busy,
    the transaction waits.
4.  **DEPART:** Records a transaction leaving a queue. It is generally
    used after the transaction obtains the required resource.
5.  **ADVANCE:** Delays a transaction for a specified amount of
    simulated time. It can represent service or processing time.
6.  **RELEASE:** Frees a facility so that another transaction can use
    it.
7.  **TERMINATE:** Removes a transaction from the simulation. Its
    operand may reduce the termination counter used to end a run.

### Typical sequence

``` text
GENERATE
   |
 QUEUE
   |
 SEIZE
   |
 DEPART
   |
 ADVANCE
   |
 RELEASE
   |
TERMINATE
```

### Working

-   First, `GENERATE` creates a customer.
-   `QUEUE` records the customer joining the waiting line.
-   `SEIZE` tries to capture the service counter.
-   After the counter is obtained, `DEPART` records leaving the queue.
-   `ADVANCE` represents the service duration.
-   `RELEASE` makes the counter available.
-   `TERMINATE` removes the customer from the model.

**Hinglish summary:** Ye blocks GPSS ke basic commands hain. Inka
sequence customer ke complete journey ko show karta hai---arrival,
waiting, service aur departure.

------------------------------------------------------------------------

## Q4. What is action time in GPSS? Explain its types.

### Answer

**Action time** is the amount of simulated time required for a
transaction to complete an activity or remain delayed in a process.

In GPSS, the `ADVANCE` block is commonly used to represent the time
taken by an activity.

### Types of action time

1.  **Constant action time:** Every transaction takes the same amount of
    time.
    -   Example: Every customer takes exactly 4 minutes for service.
2.  **Variable action time:** The time changes from one transaction to
    another.
    -   Example: Customers take different amounts of time depending on
        their requirements.
3.  **Zero action time:** An activity takes no simulated time. The
    transaction moves to the next operation without a time delay.

### Example

``` text
ADVANCE 4
```

This represents a delay of 4 simulation time units.

If the service time varies, a suitable variable or distribution-based
expression may be used, depending on the GPSS version and model.

### Importance

-   Represents processing and service durations.
-   Determines when transactions become ready for their next activity.
-   Affects queue length and waiting time.
-   Influences resource utilization and total simulation time.

**Hinglish summary:** Action time ka matlab kisi activity ko complete
karne mein lagne wala simulated time hai. Ye fixed, variable ya zero ho
sakta hai. GPSS mein `ADVANCE` delay represent karta hai.

------------------------------------------------------------------------

## Q5. Explain succession of events in GPSS.

### Answer

**Succession of events** means the order in which events are processed
during a simulation run.

In a discrete-event simulation, the simulation clock generally moves
from one scheduled event time to the next. Events are processed
according to their scheduled times.

### Working

1.  Transactions are created or scheduled for future activities.
2.  The simulation system maintains events according to their scheduled
    occurrence times.
3.  The event with the earliest scheduled time is processed next.
4.  The simulation clock advances to that event's time.
5.  The event changes the state of the system and may schedule more
    events.
6.  The process continues until the stopping condition is reached.

### Example

Suppose a customer arrives at time 2 and completes service at time 7.
Another customer arrives at time 4.

The events are processed in chronological order:

    Time Event
  ------ ----------------------------------
       2 First customer arrives
       4 Second customer arrives
       7 First customer completes service

### Importance

-   Maintains correct chronological order.
-   Avoids checking every possible instant when no event occurs.
-   Helps represent arrivals, service completions, and resource changes.
-   Makes discrete-event simulation efficient.

**Hinglish summary:** Succession of events ka matlab events ko unke
scheduled time ke order mein process karna hai. Simulation clock next
event ke time par jump karta hai.

------------------------------------------------------------------------

## Q6. Explain choice of paths in GPSS.

### Answer

**Choice of paths** refers to deciding which route a transaction should
follow while moving through a simulation model.

In a real system, different entities may follow different routes
depending on conditions, availability of resources, or probability.

### Common ways to select paths

1.  **Unconditional path:** Every transaction follows the same specified
    route.
2.  **Conditional path:** The route depends on a condition, such as
    whether a machine or counter is available.
3.  **Random or probability-based path:** A transaction is sent along
    one of multiple routes according to specified probabilities.

### Example: Two bank counters

A bank has two counters. A customer may be directed to Counter A if it
is available; otherwise, the customer may go to Counter B or wait.

``` text
             Customer
                 |
          Check Counter A
             /       \
        Available   Busy
            |         |
       Counter A   Counter B
```

### Importance

-   Represents alternative routes in real systems.
-   Helps model decision-making.
-   Allows comparison of different routing policies.
-   Supports modeling of parallel service facilities.

**Hinglish summary:** Choice of paths decide karta hai ki transaction
model mein kis route par jayega. Route fixed, condition-based ya
probability-based ho sakta hai.

------------------------------------------------------------------------

## Q7. What are conditional transfers in GPSS? Explain with an example.

### Answer

A **conditional transfer** is a mechanism used to change the path of a
transaction based on a specified condition.

In GPSS, the `TRANSFER` block is used to control the movement of
transactions. Depending on the GPSS form used, it can support
unconditional, probabilistic, or conditional routing.

### Example: Bank counter availability

Suppose a customer arrives at a bank. If Counter A is available, the
customer should go to Counter A. If it is busy, the customer should
follow another route or wait.

``` text
             Customer Arrives
                    |
             Check Availability
                /       \
            Available    Busy
                |          |
           Counter A    Alternative
```

### Steps

1.  A customer enters the system.
2.  The model checks the required condition.
3.  If the condition is satisfied, the transaction follows the first
    route.
4.  Otherwise, it follows the alternative route.
5.  The transaction continues through the selected service process.

### Importance

-   Models decisions in real systems.
-   Supports alternative processing routes.
-   Helps represent resource availability.
-   Makes simulation models more realistic.

**Note:** Exact `TRANSFER` operands and conditional syntax depend on the
GPSS version. In an exam, explain the purpose and show the routing logic
clearly if the exact dialect is not specified.

**Hinglish summary:** Conditional transfer mein transaction condition ke
according route change karta hai. Jaise counter free hai to customer
udhar jayega, busy hai to alternate route follow karega.

------------------------------------------------------------------------

## Q8. Explain GPSS program control statements: SIMULATE, RESET, CLEAR, JOB, START and END.

### Answer

GPSS program control statements control the execution and management of
a simulation program. They are different from ordinary
transaction-processing blocks.

### Important statements

  -----------------------------------------------------------------------
  Statement                           Purpose
  ----------------------------------- -----------------------------------
  `SIMULATE`                          Indicates the beginning of a GPSS
                                      simulation model in dialects that
                                      use this statement

  `RESET`                             Resets statistical counters and
                                      statistics; it does not normally
                                      remove active transactions

  `CLEAR`                             Clears the current model's
                                      statistical and transaction state,
                                      according to the GPSS dialect

  `JOB`                               Used in some GPSS dialects to end
                                      or separate one simulation job and
                                      begin another

  `START`                             Starts the simulation run and sets
                                      the termination counter

  `END`                               Marks the end of the GPSS source
                                      program
  -----------------------------------------------------------------------

### START statement example

``` text
START 100
```

This starts the simulation with a termination counter of 100. If
transactions execute `TERMINATE 1`, the counter is reduced by one for
each such transaction. The run ends when the counter reaches zero.

### Difference between RESET and CLEAR

-   **RESET:** Primarily resets statistical information while the
    model's active transactions continue.
-   **CLEAR:** Performs a broader clearing of the current simulation
    state, including transactions, depending on the GPSS implementation.

### Importance

These statements help the programmer initialize, run, reset, and finish
simulation experiments.

**Version note:** The precise availability and effects of `SIMULATE`,
`JOB`, `CLEAR`, and `RESET` vary across GPSS implementations. Use the
definitions and syntax prescribed in your class notes or textbook if
they differ.

**Hinglish summary:** Program control statements simulation ko start,
reset, clear aur end karne ke liye hote hain. `START` run begin karta
hai, aur termination counter zero hone par run stop ho sakta hai.

------------------------------------------------------------------------

## Q9. Explain the organization of a SIMSCRIPT program.

### Answer

**SIMSCRIPT** is a high-level simulation programming language used to
describe and study complex systems. It supports the representation of
entities, events, activities, and system logic.

A SIMSCRIPT program is commonly explained through three major parts:

### 1. Preamble

The preamble contains declarations and definitions required by the
program.

It may define: - Variables and attributes. - Sets and entities. -
Resources and other model data. - Required data structures.

### 2. Main program

The main program controls the initial execution of the simulation.

Its tasks may include: - Initializing variables. - Setting initial
conditions. - Creating initial entities. - Scheduling the first
events. - Starting or controlling the simulation run.

### 3. Event subprograms

Event subprograms describe what happens when a particular event occurs.

They may: - Update the state of the system. - Change resource
availability. - Schedule future events. - Record statistics.

### General organization

``` text
        SIMSCRIPT PROGRAM
                |
        -----------------
        |       |       |
     Preamble  Main   Event
              Program Subprograms
        |       |       |
   Declarations Initialize Event logic,
   and data     model    state updates
```

### Example: Bank simulation

-   **Preamble:** Declare customer and counter-related data.
-   **Main program:** Initialize the bank and schedule the first
    customer arrival.
-   **Event subprograms:** Handle customer arrival and service
    completion.

**Hinglish summary:** SIMSCRIPT program ke three main parts hote
hain---Preamble, Main Program aur Event Subprograms. Preamble
declarations rakhta hai, Main Program initialization karta hai aur Event
Subprograms events ka logic handle karte hain.

------------------------------------------------------------------------

## Q10. Explain names and labels in SIMSCRIPT.

### Answer

In SIMSCRIPT, **names** and **labels** are used to identify program
elements and statements.

### 1. Names

Names identify variables, attributes, entities, and other program
elements.

Examples:

``` text
AGE
AB12
PERSON.AGE
```

A name should clearly indicate the purpose of the element. For example,
`AGE` may represent a person's age, while `PERSON.AGE` may refer to the
age attribute of a person entity.

### 2. Labels

A label identifies a particular statement or location in a program. It
can be used to transfer control to that point.

Example:

``` text
'NEXT.STEP'
```

A statement label is written in the format supported by the SIMSCRIPT
version being used. In classic SIMSCRIPT examples, labels may be
enclosed in single quotation marks and used with a control-transfer
statement such as `GO TO`.

### Difference between names and labels

  -----------------------------------------------------------------------
  Names                               Labels
  ----------------------------------- -----------------------------------
  Identify program elements such as   Identify a statement or location in
  variables or attributes             the program

  Used to refer to data or entities   Used to refer to a point in program
                                      control

  Example: `AGE`                      Example: `'NEXT.STEP'`
  -----------------------------------------------------------------------

**Hinglish summary:** Names variables aur attributes ko identify karte
hain. Labels program ke kisi statement ya location ko identify karte
hain, jahan control transfer ho sakta hai.

------------------------------------------------------------------------

## Q11. Explain important statements used in SIMSCRIPT.

### Answer

SIMSCRIPT uses statements to perform calculations, modify values, make
decisions, repeat operations, read data, and control program execution.

The following are commonly taught statement forms. Exact syntax may vary
by SIMSCRIPT version.

  -----------------------------------------------------------------------
  Statement                           Purpose
  ----------------------------------- -----------------------------------
  `LET`                               Assigns a value to a variable

  `ADD`                               Adds a value to a variable

  `SUBTRACT`                          Subtracts a value from a variable

  `IF`                                Tests a condition and selects an
                                      action

  `GO TO`                             Transfers control to a labeled
                                      statement

  `FOR`                               Repeats a group of statements

  `READ`                              Accepts or reads input data

  `PRINT`                             Displays output

  `STOP`                              Stops execution or a simulation run

  `END`                               Marks the end of a program or
                                      program unit, as defined by the
                                      dialect
  -----------------------------------------------------------------------

### Explanation with simple examples

1.  **LET:** Used to assign a value.
    -   Example idea: Set `COUNT` to 10.
2.  **ADD:** Increases a variable by a given amount.
    -   Example idea: Add 1 to `COUNT`.
3.  **SUBTRACT:** Decreases a variable by a given amount.
    -   Example idea: Subtract 1 from `COUNT`.
4.  **IF:** Checks whether a condition is true.
    -   Example idea: If the queue length is greater than 5, take
        another action.
5.  **GO TO:** Transfers control to a labeled location.
6.  **FOR:** Repeats a set of statements for a range or collection.
7.  **READ:** Takes input values for the program.
8.  **PRINT:** Displays results such as average waiting time.
9.  **STOP:** Stops the execution when the required condition is
    reached.
10. **END:** Indicates the end of the relevant program unit.

### Importance

These statements provide the basic programming facilities needed to
build simulation logic in SIMSCRIPT.

**Syntax note:** SIMSCRIPT II.5 and other versions have specific
grammar. For example, conditionals and loops may use version-specific
forms such as `IF ... ENDIF` and `FOR ... DO ... LOOP`. Treat the
examples above as explanations of statement purpose, not as a complete
version-independent program.

**Hinglish summary:** SIMSCRIPT statements programming ke basic
operations perform karte hain---value assign karna, add/subtract karna,
condition check karna, loop chalana, input lena aur output print karna.

------------------------------------------------------------------------

## Q12. Differentiate between GPSS and SIMSCRIPT.

### Answer

GPSS and SIMSCRIPT are both simulation languages, but they represent and
organize simulation models differently.

  -----------------------------------------------------------------------
  GPSS                                SIMSCRIPT
  ----------------------------------- -----------------------------------
  General Purpose Simulation System   High-level simulation programming
                                      language

  Commonly uses a                     Uses program structures, entities,
  transaction-and-block approach      events, and statements

  Transactions move through           Model logic is expressed through
  predefined blocks                   program statements and event
                                      routines

  Provides standard blocks such as    Uses statements and subprograms to
  `GENERATE`, `SEIZE`, and `ADVANCE`  describe model behaviour

  Often convenient for queueing and   Suitable for describing a broad
  service-system models               range of complex simulation models

  Model flow is strongly represented  Program organization is commonly
  by block sequences                  explained through preamble, main
                                      program, and event subprograms
  -----------------------------------------------------------------------

### Conclusion

GPSS is useful when a system can be represented as transactions moving
through predefined blocks. SIMSCRIPT offers a more general programming
structure for expressing simulation logic.

**Hinglish summary:** GPSS block-oriented hai---transactions blocks se
move karte hain. SIMSCRIPT program-oriented hai---declarations,
statements aur event subprograms ke through model banaya jata hai.

------------------------------------------------------------------------

# Quick Revision Sheet

## GPSS at a glance

-   GPSS = General Purpose Simulation System.
-   Main approach = transaction-oriented, block-oriented, discrete-event
    simulation.
-   Transaction = customer/job/entity.
-   Block = predefined instruction.
-   Facility = single-capacity resource.
-   Storage = multiple-capacity resource.
-   Queue = waiting line.

### Important GPSS blocks

  Block         Remember
  ------------- ----------------------------------------
  `GENERATE`    Create
  `QUEUE`       Join waiting line / record queue entry
  `SEIZE`       Capture resource
  `DEPART`      Leave queue / record queue departure
  `ADVANCE`     Delay
  `RELEASE`     Free resource
  `TERMINATE`   Remove transaction

### GPSS program control

-   `START` -- begin run and set termination counter.
-   `RESET` -- reset statistics.
-   `CLEAR` -- clear model state, as defined by the dialect.
-   `SIMULATE`, `JOB`, `END` -- program-control statements used in
    certain GPSS dialects.

## SIMSCRIPT at a glance

**Program organization:** 1. Preamble -- declarations. 2. Main Program
-- initialization and control. 3. Event Subprograms -- event processing
and state changes.

**Names:** identify variables and attributes, e.g. `AGE`.

**Labels:** identify program locations, e.g. `'NEXT.STEP'`.

**Statements:** - `LET` -- assign - `ADD` -- add - `SUBTRACT` --
subtract - `IF` -- condition - `GO TO` -- transfer control - `FOR` --
repetition - `READ` -- input - `PRINT` -- output - `STOP` -- stop -
`END` -- end

------------------------------------------------------------------------

# Last-Minute Exam Tips

1.  **GPSS basics:** Learn transaction, block, facility, storage, and
    queue with examples.
2.  **GPSS blocks:** Remember the sequence
    `GENERATE → QUEUE → SEIZE → DEPART → ADVANCE → RELEASE → TERMINATE`.
3.  **Action time:** Explain constant, variable, and zero action time;
    connect `ADVANCE` with delay.
4.  **Event succession:** Mention chronological processing and the
    simulation clock moving to the next scheduled event.
5.  **Choice of paths and conditional transfers:** Draw the two-counter
    example. It makes the answer clearer.
6.  **Control statements:** Learn the purpose of `START`, `RESET`,
    `CLEAR`, and `END`; mention that exact behaviour can depend on GPSS
    version.
7.  **SIMSCRIPT organization:** Memorize Preamble, Main Program, and
    Event Subprograms.
8.  **Names vs labels:** Prepare the comparison table.
9.  **SIMSCRIPT statements:** Learn each statement's purpose and one
    simple example idea.
10. **GPSS vs SIMSCRIPT:** Practice the comparison table for a short or
    long question.

**Most important topics to revise first:** GPSS basic concepts and
blocks, action times, succession of events, conditional transfers, GPSS
control statements, SIMSCRIPT organization, and SIMSCRIPT statements.
