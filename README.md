# CMSI 385 Final Project
## NFA Simulator
Coded in: Java   
IDE: Eclipse - Version: 2019-09 R (4.13.0)  
Implement a command line program which takes in a description of an NFA (via STDIN) and a string (via command line arg) and returns whether or not the string is accepted in the language of the NFA passed in.  

Recommended Input Format:    
START=q0; ACCEPT=q2,q1

q0:a->q1

q0:a->q2

q0->q2

q0:a->q0

Example input on command line (MacOS):
```
MacBook-Pro:nfa mayadahlke$ javac NFA.java
MacBook-Pro:nfa mayadahlke$ java NFA.java a
NFA Simulator
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The string you entered is: a
Enter a description of an NFA:
Press Command + D on OS X or Control + D on Windows when you are done.
START=q0; ACCEPT=q2,q1

q0:a->q1

q0:a->q2

q0->q2

q0:a->q0
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
start:q0
end:[q1, q2]
transitions:{q0={a=[q1, q2, q0], λ=[q2]}}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
a is an accepted string in this NFA.
```

Note: To test if the NFA accepts lambda, use this character `λ`  
e.g.`MacBook-Pro:nfa mayadahlke$ java NFA.java λ` 

## Turing Machine Simulator (Extra Credit)
Coded in: Java   
IDE: Eclipse - Version: 2019-09 R (4.13.0)  
Implement a command line program which takes in a description of a Turing Machine (via STDIN) and a string (via command line arg) and returns whether or not the string is accepted in the language of the Turing Machine passed in.  

Recommended Input Format:  
START=q0;ACCEPT=q2,q1;BLANK=B   

q0:a->b,R,q1   

q1:a->c,L,q2  

q0:b->b,R,q0  

Example input on command line (MacOS):
```
MacBook-Pro:nfa mayadahlke$ javac TuringMachine.java
MacBook-Pro:turing mayadahlke$ java TuringMachine.java ba
Turing Machine Simulator
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The string you entered is: ba
Enter a description of an NFA:
Press Command + D on OS X or Control + D on Windows when you are done.
START=q0;ACCEPT=q2,q1;BLANK=B

q0:a->b,R,q1

q1:a->c,L,q2

q0:b->b,R,q0    
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
start:q0
end:[q1, q2]
transitions:{q0={a->b,R=[q1], b->b,R=[q0]}, q1={a->c,L=[q2]}}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
ba is an accepted string in this Turing Machine.
```
