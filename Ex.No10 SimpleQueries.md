# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE: 13-09-2025                                                                         
### REGISTER NUMBER : 212223040216
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.
### Program:
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:
```
likes(john,X):-food(X). 
food(apple).
food(chicken).
eats(sue,X):-eats(bill,X).
eats(bill,peanuts). 
```


### Output:

<img width="937" height="169" alt="Screenshot 2025-09-06 141307" src="https://github.com/user-attachments/assets/8cd36167-d163-4a69-9177-3bb041625119" />


### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```
likes(steve,X):-easycourse(X).
hard(science).
easycourse(X):-dept(basketweaving,X). 
dept(basketweaving, bk301).
``` 
### Output:

<img width="936" height="162" alt="Screenshot 2025-09-06 141337" src="https://github.com/user-attachments/assets/7235eeea-a87e-4042-9bf1-3e48d343f6aa" />

### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:

```
crime(X):-
    	  american(X),
    	  weapon(Y),
    	  hostile(X,Z),
          sells(X,Y,Z).
sells(west,Y,nano):-
    owns(nano,Y),
    missile(Y). 
weapon(Y):-
    missile(A).
hostile(B,A):-
    enemy(A,B).
enemy(nano,west).
owns(nano,m1).
missile(m1).
american(west).

```
### Output:

<img width="948" height="182" alt="Screenshot 2025-09-06 143644" src="https://github.com/user-attachments/assets/7678b982-3034-467d-b6af-3b658c6abb43" />

### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
