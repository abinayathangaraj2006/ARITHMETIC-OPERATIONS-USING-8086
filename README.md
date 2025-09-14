# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations


<img width="542" height="882" alt="Screenshot 2025-09-14 180614" src="https://github.com/user-attachments/assets/5896baaf-2660-4a7a-aeb8-85620427634c" />

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="1193" height="968" alt="Screenshot 2025-09-14 175306" src="https://github.com/user-attachments/assets/af23c584-3ab5-4273-bfad-08c97fedadf7" />


<img width="1635" height="985" alt="Screenshot 2025-09-14 175231" src="https://github.com/user-attachments/assets/cd78719f-0f5c-4b3e-9ab6-13b159bddb3a" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table





## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="1577" height="1021" alt="Screenshot 2025-09-14 175332" src="https://github.com/user-attachments/assets/b63b69b9-4ad3-4b86-824a-05106e540b55" />

<img width="980" height="900" alt="Screenshot 2025-09-14 175734" src="https://github.com/user-attachments/assets/504f61cf-a806-4a64-a1ac-2d7494d7fe1b" />

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

<img width="518" height="791" alt="Screenshot 2025-09-14 181022" src="https://github.com/user-attachments/assets/b39f4496-245c-42cd-8e73-e64138e0ce46" />


## OUTPUT SCREEN FROM MASM SOFTWARE


<img width="1451" height="941" alt="Screenshot 2025-09-14 175824" src="https://github.com/user-attachments/assets/ad848407-185e-401b-8ca1-1fa6cf4efdde" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations
<img width="443" height="841" alt="Screenshot 2025-09-14 181210" src="https://github.com/user-attachments/assets/e81faab0-ed40-4fc8-989b-2c3122085d9e" />


## OUTPUT FROM MASM SOFTWARE

![Uploading Screenshot 2025-09-14 175839.png…]()


<img width="1503" height="987" alt="Screenshot 2025-09-14 175900" src="https://github.com/user-attachments/assets/5a87d525-7134-4f8e-bda4-65b0514786dc" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

