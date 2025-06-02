# Ex.No: 6   Logic Programming – Towers of Hanoi Problem   
### DATE: 25.03.2025                                                                           
### REGISTER NUMBER : 212222220019

---

### AIM: 
To write a logic program to solve the Towers of Hanoi problem using SWI-PROLOG.

---

### Algorithm:
1. Start the program.  
2. Write rules for finding the solution of the Towers of Hanoi in SWI-PROLOG.  
3.  
   a) If there is only *one disk*, move the disk from X to Y.  
   
   b) If the number of disks is greater than 1:  
   - i) Move *N-1 disks* from source peg X to auxiliary peg Z.  
   - ii) Move the *Nth disk* from source peg X to destination peg Y.  
   - iii) Move the *N-1 disks* from auxiliary peg Z to destination peg Y.  
4. Run the program to get the solution steps.  
5. Stop the program.

---

### Program:
```
prolog
% Base Case
move(1, X, Y, _) :-
    write('Move disk from '), write(X), write(' to '), write(Y), nl.

% Recursive Case
move(N, X, Y, Z) :-
    N > 1,
    N1 is N - 1,
    move(N1, X, Z, Y),
    move(1, X, Y, _),
    move(N1, Z, Y, X).

```
### Output:
![image](https://github.com/user-attachments/assets/604c89d9-9c8c-4403-9ad1-c2bd0d1bb128)

---

### Result:
Thus, the solution of the Towers of Hanoi problem was found using logic programming.
