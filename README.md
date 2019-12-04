# CMSI 385 Final Project
Maya Dahlke

## NFA Simulator
Coded in Java   
Implement a command line program which takes in a description of an NFA (via STDIN) and a string (via command line arg) and returns whether or not the string is accepted in the language of the NFA passed in.  

> Recommended Input Format:    
> START=q0; ACCEPT=q2,q1
>
> q0:a->q1
>
> q0:a->q2
>
> q0->q2
>
> q0:a->q0

Example input on command line (MacOS):
```
MacBook-Pro:nfa mayadahlke$ javac NFA.java
MacBook-Pro:nfa mayadahlke$ java NFA.java 001
NFA Simulator
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The string you entered is: 001
Enter a description of an NFA:
Press Command + D on OS X or Control + D on Windows when you are done.
ACCEPT=q0
q0:0->q1
q1:0->q2
q2:1->q0
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
start:q0
end:[q0]
transitions:{q0={0=[q1]}, q1={0=[q2]}, q2={1=[q0]}}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
001 is an accepted string in this NFA.
```

Note: for lambda moves use this character `λ`
