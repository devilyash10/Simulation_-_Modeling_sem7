# **Module V – SIMSCRIPT Statements**

Important exam topic

## **1. Introduction**

**SIMSCRIPT Statements** are instructions used to perform different operations in a SIMSCRIPT program.

They are used to assign values, perform calculations, take decisions, repeat operations, read input and display output.

SIMSCRIPT uses simple English-like statements, making programs easier to understand.

## **2. Types of SIMSCRIPT Statements**

The important statements are explained below.

### **1. LET Statement**

- The LET statement is used to assign a value to a variable.
- It can also be used to store the result of a mathematical expression.

**Example:**

```
LET A = 10
LET B = A + 5
```

Here, A is assigned 10 and B is assigned 15.

**Hinglish:** LET ka use variable mein value store ya assign karne ke liye hota hai.

### **2. ADD Statement**

- The ADD statement is used to add a value to a variable.
- It updates the existing value of that variable.

**Example:**

```
ADD 5 TO A
```

If A = 10, its new value becomes 15.

**Hinglish:** ADD kisi existing variable ki value mein number add karta hai.

### **3. SUBTRACT Statement**

- The SUBTRACT statement is used to subtract a value from a variable.
- It updates the variable with the reduced value.

**Example:**

```
SUBTRACT 3 FROM A
```

If A = 10, its new value becomes 7.

**Hinglish:** SUBTRACT variable ki existing value se number minus karta hai.

### **4. IF Statement**

- The IF statement is used to check a condition.
- If the condition is true, the specified statements are executed.
- Otherwise, the ELSE part is executed, if provided.

**Example:**

```
IF A > 10
    LET B = 1
ELSE
    LET B = 0
ENDIF
```

**Hinglish:** IF condition check karta hai. True hone par IF wala part aur false hone par ELSE wala part execute hota hai.

### **5. GO TO Statement**

- GO TO is used to transfer program control to a specified label.
- It changes the normal flow of program execution.

**Example:**

```
GO TO 'NEXT'
```

The program transfers control to the statement marked with the label `NEXT`.

**Hinglish:** GO TO program ko kisi particular label ya statement par jump karwata hai.

### **6. FOR Statement**

- FOR is used to repeat a group of statements for a specified range.
- It is useful when an operation must be performed multiple times.

**Example:**

```
FOR I = 1 TO 5
DO
    PRINT 1 LINE WITH I
LOOP
```

This prints the values from 1 to 5.

**Hinglish:** FOR loop kisi kaam ko given number of times repeat karta hai.

### **7. READ Statement**

- READ is used to accept input from the user or an input file.
- The entered values are stored in variables.

**Example:**

```
READ A
```

It reads a value and stores it in A.

**Hinglish:** READ ka use input lene ke liye hota hai.

### **8. PRINT Statement**

- PRINT is used to display output.
- It can display values, messages and calculated results.

**Example:**

```
PRINT 1 LINE WITH A
```

It displays the value of A.

**Hinglish:** PRINT screen par output show karta hai.

### **9. STOP Statement**

- STOP is used to terminate the execution of a SIMSCRIPT program.
- It can be used when a particular condition is satisfied.

**Example:**

```
IF A = 100
    STOP
ENDIF
```

**Hinglish:** STOP program ki execution ko terminate kar deta hai.

### **10. END Statement**

- END indicates the physical end of a SIMSCRIPT source program.
- It is written at the end of the program.

**Example:**

```
END
```

**Hinglish:** END program ke source code ka ending marker hota hai.

The statement descriptions and examples above follow SIMSCRIPT II.5 conventions.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www3.cs.stonybrook.edu\&sz=32)

www3.cs.stonybrook.edu+2



## **3. Difference Between Important SIMSCRIPT Statements**

| Statement | Purpose                    |
| --------- | -------------------------- |
| LET       | Assign a value             |
| ADD       | Add a value                |
| SUBTRACT  | Subtract a value           |
| IF        | Check a condition          |
| GO TO     | Transfer control           |
| FOR       | Repeat statements          |
| READ      | Accept input               |
| PRINT     | Display output             |
| STOP      | Terminate execution        |
| END       | Mark end of source program |

## **4. Example of a Simple SIMSCRIPT Program**

**Program to add two numbers:**

```
BEGIN
    READ A, B
    LET SUM = A + B
    PRINT 1 LINE WITH SUM
END
```

**Explanation:**

1. READ accepts two numbers.
2. LET calculates their sum.
3. PRINT displays the result.
4. END marks the end of the program.

This is a simplified illustration of the statement concepts, not a complete SIMSCRIPT II.5 program structure.

## **5. Advantages of SIMSCRIPT Statements**

1. Easy to understand because of English-like syntax.
2. Supports mathematical calculations.
3. Allows decision-making using IF statements.
4. Supports repetition using loops.
5. Helps control program execution.
6. Supports input and output operations.

## **6. Conclusion**

SIMSCRIPT statements are used to perform operations and control program execution. Statements such as LET, ADD, SUBTRACT, IF, GO TO, FOR, READ and PRINT help develop simulation programs in a simple and organized way.

## **Quick Revision – Hinglish Summary 📝**

| Statement | Easy meaning             |
| --------- | ------------------------ |
| LET       | Value assign karna       |
| ADD       | Value add karna          |
| SUBTRACT  | Value minus karna        |
| IF        | Condition check karna    |
| GO TO     | Label par jump karna     |
| FOR       | Repeat karna             |
| READ      | Input lena               |
| PRINT     | Output dikhana           |
| STOP      | Program execution rokna  |
| END       | Source program end karna |

## **Important Exam Questions**

1. What are SIMSCRIPT statements? Explain their different types with examples.
2. Explain LET, ADD and SUBTRACT statements.
3. Explain IF and GO TO statements with examples.
4. Explain FOR loop in SIMSCRIPT.
5. Explain READ, PRINT, STOP and END statements.
6. Write a short note on the important statements used in SIMSCRIPT.

**Exam tip:** Focus especially on LET, IF, GO TO, FOR, READ and PRINT. Learn their purpose and one simple example each.

Module V syllabus completed

You have now covered all the listed topics of Module V, including GPSS and SIMSCRIPT.