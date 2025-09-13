# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE: 13-09-2025                                                                            
### REGISTER NUMBER : 212223040216
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.

### Program:
```
halfadder(X,Y,Sum,Carry):-
xor(X,Y,Sum),
and(X,Y,Carry).
halfsub(X,Y,Diff,Borrow):-
	xor(X,Y,Diff),
	not(X,Z),
	and(X,Y,Borrow).
fulladd(X,Y,Z,Sum,Carry):- 
	xor(X,Y,A),
	xor(A,Z,Sum),
	and(A,Z,B),
	and(X,Y,C),
	or(B,C,Carry).
xor(0,0,0).
xor(0,1,1).
xor(1,0,1).
xor(1,1,0).
and(0,0,0).
and(0,1,0).
and(1,0,0).
and(1,1,1).
or(0,1,1).
or(0,0,0).
or(1,0,1).
or(1,1,1).
not(0,1).
not(1,0).
```

### Output:
<img width="452" height="161" alt="image" src="https://github.com/user-attachments/assets/3fa0d202-f068-427d-bef1-ac641fe5dc4f" /> 
<img width="937" height="166" alt="{4F9C0349-91B0-4F4C-99FA-3A08217D76AB}" src="https://github.com/user-attachments/assets/46694718-0ff4-41e6-9611-b4d6df1fa9d6" />
<img width="934" height="184" alt="image" src="https://github.com/user-attachments/assets/64106b65-5bcd-4ad8-b0b3-77bfe19c1290" />






### Result:
Thus the truth table of circuit verified sucessfully.
