# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE:01-04-2025                                                                            
### REGISTER NUMBER:212222040027 
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. **Start** the program.  
2. Design an **AND gate**: If both inputs are 1, output is 1.  
3. Design an **OR gate**: If any one input is 1, output is 1.  
4. Design an **XOR gate**: If inputs differ, output is 1.  
5. Design a **NOT gate**: If input is 0, output is 1 (and vice versa).  
6. Using the above gates, define logic for:  
   - **Half Adder** (Sum and Carry)  
   - **Half Subtractor** (Difference and Borrow)  
7. Test the logic with all input combinations.  
8. **Stop** the program.


### Program:
```
% Half Adder
halfadder(X, Y, Sum, Carry) :-  
    xor(X, Y, Sum),  
    and(X, Y, Carry).  

% Half Subtractor
halfsubtractor(X, Y, Difference, Borrow) :-  
    xor(X, Y, Difference),  
    not(X, NA),  
    and(NA, Y, Borrow).  

% AND Gate
and(0, 0, 0).  
and(0, 1, 0).  
and(1, 0, 0).  
and(1, 1, 1).  

% XOR Gate
xor(0, 0, 0).  
xor(0, 1, 1).  
xor(1, 0, 1).  
xor(1, 1, 0).  

% NOT Gate
not(0, 1).  
not(1, 0).
```

### Output:
![image](https://github.com/user-attachments/assets/9ac7fb1f-6bed-48ca-9256-250962e23235)



### Result:
Thus the truth table of circuit verified sucessfully.
