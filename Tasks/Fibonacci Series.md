**Fibonacci Series**
A series of numbers in which each number(Fibonacci number) is the sum of the two preceding numbers. The simplest is the series 1, 1, 2, 3, 5, 8 etc.

Write a recursive function for determining the Nth element of the Fibonacci sequence.

My initial solution:

    public static int fib(int nthOfSequence) {  
        if (nthOfSequence == 2 || nthOfSequence == 1) {  
            return 1;  
        }  
      
        return fib(nthOfSequence - 1) + fib(nthOfSequence - 2);  
    }

The solution can be improved by raising exception when user input negative value.
