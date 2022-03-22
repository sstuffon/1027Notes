# CS 1027 LECTURE: Recursive Programming

`public static void main {}`





**Examples of recursive programming**
- Consider computing the sum of all the numbers between 1 and n

1 + 2+ 3 + 4 + ... + n

Recursive definition
- First compute the sum of numbers from n+1 to 1 then we add n to that
- Sum of 1 = 1


**Recursive Algorithm*
- Need the base case and the recursive case
- Base case happens when n = 1
- The sum of 1 to n : 
    - n -1 for everthing greater than the base case (1)

- Recursive algorithm for the problem:

`Algorithm sum(n) 
 In: Positive value n
 Out: 1+...+n`
 
 Java implenttation
 `public static void main (String[] args {
    int result = sum(3)
}
    `
`public static int sum(int n) { 
if n == 1 return 1;
else return n + sum(n-1)}`


Execution stack:
- when the program starts execution it stores it in the execution record (the first address)
- ER 1: 
    - args = null
    - result = 
    - setaddr = o.s.
        - when execution finishes program will go back to the previous system

- ER 2:
    - n = 3
    - setaddr: addr1
        - when the call is called the address changes and it will be added to the executions tack

- always refer to the one at the top of the stack when comparing the multiple n values since they are stacked


**Recursion vs Iterative**
- Recursion uses more memoraty than an iterative method since you need to time to create the activation records 
- Times where recursion might not be used
    - suppose you had two small bunnies that will grow, after 1 month and then they mate
    - After 1 month, babies are born, now you have have 4 rabbits
    - After another month, the babies grow up and mate, and the og couple mate aagain --> you will have 3 pairs of rabbits
    - Another month passes: now 5 rabbits
    - Fibonnaci sequences
    - So how many rabbits will after n months?
    - 


Fibonacci Sequence
- fib(1) = 1
- fib(2) = 1
- fib(n) = fib(n-1) + fib(n-2) for n>2

`public static int fib(int term) {
		if (term == 0 || term == 1) {
			return term;
		}
		else {
			return fib(term-1) + fib(term-2); 
		}'

