## Aim
To write and execute an Assembly Language Program for sorting data in Ascending and  descending order using 8051 microcontroller on Keil software.
---

## Apparatus Required
- Personal Computer  
- Keil µVision software  
---

## Algorithm(ASCENDING ORDER)
1. Initialize the register **R7** with count (number of elements).  
2. Get the first two elements into two registers.  
3. Compare the two elements:  
   - If the value in register **R0** is lower, exchange **A** and **R0** data.  
   - Otherwise, increment pointer and decrement register **R7**.  
4. Check if **R7 = 0** → if yes, move the register **R0 & A**.  
5. Increment pointer and decrement **R7**.  
6. If **R7 ≠ 0**, repeat from Step 2.  
7. Otherwise, stop the program.  
---

## Program (Ascending order)

```asm
ORG 0000H

        MOV R4,#04H

AGAIN:  MOV R3,#04H
        MOV R0,#30H

LOOP1:  MOV A,@R0
        MOV B,A
        INC R0
        MOV A,@R0
        CJNE A,B,CONTINUE

CONTINUE:
        JNC SKIP
        MOV @R0,B
        DEC R0
        MOV @R0,A
        INC R0

SKIP:   DJNZ R3,LOOP1
        DJNZ R4,AGAIN

STOP:   SJMP STOP

END
```
## OUTPUT(Ascending order)



---

## Algorithm(Descending order)
1. Initialize the register **R7** with count.  
2. Get first two elements in two registers.  
3. Compare the two elements of data:  
   - If the value of **R0** register is high, then exchange **A** and **R0** data.  
   - Else, increment pointer and decrement register **R7**.  
4. Check if **R7 = 0**, then move the contents of **R0** and **A**.  
5. Again increment pointer and decrement **R7**.  
6. Check if **R7 = 0**:  
   - If **No**, repeat the process from Step 2.  
   - If **Yes**, stop the program.  
---
## Program (Descending order)

```asm




```
## OUTPUT(Descending order)



---
## RESULT:
Thus the sorting of given data was done using 8051 keil software.

