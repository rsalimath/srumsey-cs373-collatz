The purpose of this project is to familiarize students in Glenn Downing's CS 373-Software Engineering course.

The Collatz conjecture proposes that a number can be reduced to the value '1' through a series of calculations:

If the number is odd, multiply the number by three and add one.
If the number is even, divide the number by 2.
If the number is one, the process is complete.

The code developed for this project will take in two integer parameters that will serve as the starting and ending points in a range. Starting at the first number, the program calculates the cycle length produce when the Collatz conjecture is applied and will do the same for each number until it reaches the second number, or end point. While the program does this, it will also keep track of the maximum cycle length seen in the range.

Once this number is determined, the program will output the first and second numbers that it took in as parameters and on the same line will output the maximum cycle length seen.