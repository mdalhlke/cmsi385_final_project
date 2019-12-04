# CMSI 385 Final Project
## NFA Simulator
Coded in: Java   
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
MacBook-Pro:nfa mayadahlke$ 
```

Note: To test if the NFA accepts lambda, use this character `λ`  
e.g.`MacBook-Pro:nfa mayadahlke$ java NFA.java λ` 
