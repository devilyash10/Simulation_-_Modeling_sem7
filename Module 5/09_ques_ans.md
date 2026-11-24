# **SIMSCRIPT Statements – Important Exam Questions**

## **Q1. What are SIMSCRIPT statements? Explain their different types with examples.**

**Answer (English):**

SIMSCRIPT statements are instructions used in a SIMSCRIPT program to perform different operations. They control the execution of a program, perform calculations, accept input, display output, and manage the flow of execution.

The important types of SIMSCRIPT statements are:

1. **Assignment Statement (LET):** Used to assign a value to a variable.
   ```
   LET A = 10
   ```
2. **Arithmetic Statements (ADD and SUBTRACT):** Used to perform mathematical operations.
   ```
   ADD 5 TO A
   SUBTRACT 2 FROM A
   ```
3. **Conditional Statement (IF):** Used to execute instructions based on a condition.
   ```
   IF A > 10
       LET B = 1
   ELSE
       LET B = 0
   ENDIF
   ```
4. **Control Transfer Statement (GO TO):** Used to transfer program execution to a specified label.
   ```
   GO TO 'NEXT'
   ```
5. **Looping Statement (FOR):** Used to repeat a set of instructions.
   ```
   FOR I = 1 TO 5 DO
       PRINT 1 LINE WITH I
   LOOP
   ```
6. **Input Statement (READ):** Used to accept data from the user.
   ```
   READ A
   ```
7. **Output Statement (PRINT):** Used to display results.
   ```
   PRINT 1 LINE WITH A
   ```
8. **Termination Statements (STOP and END):** STOP terminates program execution, while END indicates the end of the program.

**Conclusion:** SIMSCRIPT statements make it possible to perform calculations, take decisions, repeat operations, handle input/output, and control program execution.

**Hinglish Summary:** SIMSCRIPT statements program ko instructions dete hain. Inki help se hum values assign karte hain, calculations karte hain, conditions check karte hain, loops chalate hain aur program ko start/stop ya control karte hain.

## **Q2. Explain LET, ADD and SUBTRACT statements.**

**Answer (English):**

These statements are used to perform basic operations on variables in SIMSCRIPT.

**1. LET Statement**

- LET is an assignment statement.
- It assigns a value or result of an expression to a variable.

Example:

```
LET A = 10
LET B = A + 5
```

Here, A is assigned 10 and B is assigned 15.

**2. ADD Statement**

- ADD is used to add a value to an existing variable.
- The result is stored in the same variable.

Example:

```
LET A = 10
ADD 5 TO A
```

Result: A = 15.

**3. SUBTRACT Statement**

- SUBTRACT is used to subtract a value from an existing variable.
- The result is stored in the same variable.

Example:

```
LET A = 10
SUBTRACT 3 FROM A
```

Result: A = 7.

| Statement | Purpose           | Example             |
| --------- | ----------------- | ------------------- |
| LET       | Assigns a value   | `LET A = 10`        |
| ADD       | Adds a value      | `ADD 5 TO A`        |
| SUBTRACT  | Subtracts a value | `SUBTRACT 3 FROM A` |

**Hinglish Summary:** LET value assign karta hai, ADD existing value mein number jodta hai aur SUBTRACT existing value mein se number ghataata hai.

## **Q3. Explain IF and GO TO statements with examples.**

**Answer (English):**

**1. IF Statement**

The IF statement is a conditional statement used to check whether a condition is true or false. Instructions are executed according to the result of the condition.

Example:

```
LET A = 15

IF A > 10
    PRINT 1 LINE WITH "A is greater than 10"
ELSE
    PRINT 1 LINE WITH "A is not greater than 10"
ENDIF
```

Here, the condition A > 10 is true, so the first message is displayed.

**2. GO TO Statement**

The GO TO statement is used to transfer program control from one statement to another specified label. It helps in changing the normal sequence of program execution.

Example:

```
GO TO 'NEXT'

PRINT 1 LINE WITH "Hello"

'NEXT'
PRINT 1 LINE WITH "Welcome"
```

Here, control directly moves to the label `NEXT`, so the program displays "Welcome".

**Difference:**

| IF Statement                                             | GO TO Statement                           |
| -------------------------------------------------------- | ----------------------------------------- |
| Checks a condition.                                      | Transfers program control.                |
| Executes instructions based on true or false conditions. | Transfers execution to a specified label. |
| Used for decision-making.                                | Used for changing execution flow.         |

**Hinglish Summary:** IF condition check karta hai aur uske according decision leta hai. GO TO program ko directly kisi specified label par le jaata hai.

## **Q4. Explain FOR loop in SIMSCRIPT.**

**Answer (English):**

The FOR loop is a looping statement in SIMSCRIPT. It is used to execute a group of statements repeatedly for a specified number of times.

It reduces code repetition and makes programs easier to write and understand.

**Syntax:**

```
FOR variable = starting_value TO ending_value DO
    statements
LOOP
```

**Example:**

```
FOR I = 1 TO 5 DO
    PRINT 1 LINE WITH I
LOOP
```

**Output:**

```
1
2
3
4
5
```

**Working:**

1. The loop starts with I = 1.
2. The statements inside the loop are executed.
3. The value of I increases for the next iteration.
4. The loop continues until the specified ending value is reached.

**Advantages:**

- Reduces repeated code.
- Saves programming time.
- Makes programs easier to understand.
- Useful for performing repetitive simulation tasks.

**Hinglish Summary:** FOR loop kisi statement ko baar-baar execute karta hai. Jaise FOR I = 1 TO 5 ka matlab hai ki loop 1 se 5 tak chalega aur har baar I ki value change hogi.

## **Q5. Explain READ, PRINT, STOP and END statements.**

**Answer (English):**

These statements are used for input, output, and termination of a SIMSCRIPT program.

**1. READ Statement**

- READ is used to accept input data.
- It stores the entered value in a variable.

Example:

```
READ A
```

It accepts a value and stores it in variable A.

**2. PRINT Statement**

- PRINT is used to display information or results.
- It can display variable values and messages.

Example:

```
LET A = 20
PRINT 1 LINE WITH A
```

Output: 20.

**3. STOP Statement**

- STOP is used to terminate the execution of a program.
- It stops further execution of the program.

Example:

```
STOP
```

**4. END Statement**

- END indicates the end of the SIMSCRIPT source program.
- It marks the end of the program's statements.

Example:

```
PRINT 1 LINE WITH "Program Completed"
END
```

**Difference between STOP and END:**

| STOP                               | END                                  |
| ---------------------------------- | ------------------------------------ |
| Terminates program execution.      | Marks the end of the source program. |
| Used as a termination instruction. | Used to indicate the program's end.  |

**Hinglish Summary:** READ input leta hai, PRINT output show karta hai, STOP program execution rokta hai aur END source program ke end ko indicate karta hai.

## **Q6. Write a short note on the important statements used in SIMSCRIPT.**

**Answer (English):**

SIMSCRIPT provides several statements to control program execution and perform different operations. The important statements are:

1. **LET:** Assigns a value to a variable.
2. **ADD:** Adds a value to an existing variable.
3. **SUBTRACT:** Subtracts a value from a variable.
4. **IF:** Checks a condition and performs an action accordingly.
5. **GO TO:** Transfers control to a specified label.
6. **FOR:** Repeats a group of statements.
7. **READ:** Accepts input data.
8. **PRINT:** Displays output.
9. **STOP:** Terminates program execution.
10. **END:** Indicates the end of the source program.

These statements are useful for calculations, decision-making, looping, input/output operations, and controlling the execution of simulation programs.

**Hinglish Summary:** SIMSCRIPT ke important statements program ke different tasks perform karte hain—LET, ADD aur SUBTRACT calculations ke liye; IF aur GO TO control ke liye; FOR repetition ke liye; READ aur PRINT input-output ke liye; aur STOP aur END termination ke liye.

## **Quick Revision – Learn Before the Exam**

| Statement | Remember it as        |
| --------- | --------------------- |
| LET       | Assign a value        |
| ADD       | Addition              |
| SUBTRACT  | Subtraction           |
| IF        | Decision-making       |
| GO TO     | Jump to a label       |
| FOR       | Repetition / Loop     |
| READ      | Input                 |
| PRINT     | Output                |
| STOP      | Stop execution        |
| END       | End of source program |

**Exam tip:** Q1 and Q6 overlap significantly. Prepare Q1 properly and you can easily write Q6. Also learn the examples of LET, IF, FOR and GO TO because they are useful in separate questions.