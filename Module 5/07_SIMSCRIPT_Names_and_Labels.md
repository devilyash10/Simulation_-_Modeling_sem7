# **Module V – SIMSCRIPT Names and Labels**

## **1. Names in SIMSCRIPT**

**Definition:** Names in SIMSCRIPT are identifiers used to identify variables, attributes and other program elements.

They help programmers store and access information in a simulation program.

### **Rules for Names**

1. A name can contain letters and digits.
2. A name must contain at least one letter.
3. A period (`.`) can also be used in names.
4. Names should be meaningful and easy to understand.
5. Special SIMSCRIPT names should not be used incorrectly.

**Examples:**

| Valid Names | Meaning           |
| ----------- | ----------------- |
| AGE         | Age variable      |
| AB12        | Alphanumeric name |
| PERSON.AGE  | Age of a person   |
| TOTAL       | Total value       |
| PART.NUMBER | Part number       |

**Hinglish Summary:** Names ka use variables aur attributes ko identify karne ke liye hota hai. Name mein letters, digits aur dot use kar sakte hain, lekin at least ek letter hona zaroori hai.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://archive.cs.rutgers.edu\&sz=32)

archive.cs.rutgers.edu+1



## **2. Labels in SIMSCRIPT**

**Definition:** Labels are identifiers used to mark specific statements in a program. They help transfer program control from one statement to another using the `GO TO` statement.

### **Rules for Labels**

1. Labels are written inside single quotation marks (`' '`).
2. They can contain letters, digits and periods.
3. A label identifies a particular statement.
4. Labels are used with the `GO TO` statement.
5. Labels are local to the routine in which they are defined.

**Examples:**

```
'LABEL1'
'AB12'
'1234'
'ERROR.13'
'WRITE.OUTPUT'
```

**Hinglish Summary:** Label ek statement ka naam ya address hota hai. Iska use `GO TO` ke through program control ko kisi specific statement par bhejne ke liye hota hai.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www3.cs.stonybrook.edu\&sz=32)

www3.cs.stonybrook.edu+1



## **3. Subscripted Labels**

A label can also have a subscript, which is a positive integer written in parentheses immediately after the label name.

**Examples:**

```
'PLACE(3)'
'INPUT.CARD(32)'
'X(1)'
```

Subscripted labels are useful when a program contains multiple transfer points with the same label name.

They allow programmers to add or remove labelled statements without changing all the corresponding `GO TO` statements.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www3.cs.stonybrook.edu\&sz=32)

www3.cs.stonybrook.edu



## **4. Difference Between Names and Labels**

| Basis          | Names                     | Labels                    |
| -------------- | ------------------------- | ------------------------- |
| Meaning        | Identify program elements | Identify statements       |
| Main use       | Variables and attributes  | Control transfer          |
| Format         | Written normally          | Enclosed in single quotes |
| Special symbol | Period can be used        | Period can be used        |
| Example        | PERSON.AGE                | 'PERSON.AGE'              |
| Used with      | Variables and attributes  | GO TO statement           |

## **5. Example**

```
LET AGE = 22
GO TO NEXT.STEP

'NEXT.STEP'
PRINT 1 LINE WITH AGE
```

**Explanation:**

- `AGE` is a variable name.
- `'NEXT.STEP'` is a label.
- `GO TO NEXT.STEP` transfers control to the statement identified by that label.
- The program then prints the value of AGE.

## **6. Advantages of Names and Labels**

1. Make programs easier to understand.
2. Help identify variables and statements.
3. Improve program organization.
4. Help transfer control between statements.
5. Make program modification easier.

## **7. Conclusion**

Names and labels are important elements of SIMSCRIPT. Names identify variables and attributes, whereas labels identify statements and help control program execution through the `GO TO` statement.

## **Quick Revision 📝**

**Names**

- Identify variables and attributes.
- Must contain at least one letter.
- Example: `PERSON.AGE`

**Labels**

- Identify program statements.
- Written inside single quotation marks.
- Used with `GO TO`.
- Example: `'NEXT.STEP'`

**Subscripted Labels**

- Label followed by a positive integer in parentheses.
- Example: `'PLACE(3)'`

## **Important Exam Questions**

1. Define Names in SIMSCRIPT and explain their naming rules.
2. What are Labels in SIMSCRIPT? Explain their rules with examples.
3. Explain Subscripted Labels with examples.
4. Differentiate between Names and Labels in SIMSCRIPT.



Exam tip

&#x20;The most important distinction to remember is: **Names identify variables; Labels identify statements.**



**Next topic: SIMSCRIPT Statements** — the final topic of Module V.