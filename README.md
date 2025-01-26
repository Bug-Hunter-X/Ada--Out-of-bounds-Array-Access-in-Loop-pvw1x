# Ada Out-of-Bounds Array Access Bug

This repository demonstrates a common error in Ada programming: accessing an array element outside its defined bounds.  The code attempts to double each element of an array, but the loop index goes beyond the array's last element causing a runtime error.  The solution shows how to correctly iterate within the array's bounds.

## Bug Description
The `Example` procedure uses a `for` loop to iterate through an array. However, inside the loop, `My_Arr(I + 1)` attempts to access an element one position beyond the actual array size. This results in a runtime exception, typically a `Constraint_Error`.  This is a subtle bug because the code seems correct at first glance, especially for programmers coming from languages that don't have strict array bounds checking.

## Solution
The solution modifies the loop to iterate correctly, ensuring that the index always remains within the bounds of the array. 