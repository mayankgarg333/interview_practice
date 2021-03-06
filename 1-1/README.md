## Solution of problem 1.1

**Q. Implement an algorithm to determine if a string has all unique characters. What if you can not use additional data structures?**

**Sol.** 
If we are allowed to use extra data structure then we can simply use a hash map and store each element in the map. Then traverse the map and look for the frequency of the each element. If all elements have frequency of 1 then it is unique otherwise not unique. 

If no extra data structure is allowed 

**method 1** 

Sort the string and check if any element is repeated. 
O(n log n)

**method 2** 

compare each element with rest of the string array. 
O(n^2)

**Using fixed extra space**

1. Use array of length 128 (if ASCII code string) to store the repetition of the characters. And map the ASCII code of the character to the value of the array. If value is greater than 1 anytime, then not unique. Also is the string length is greater than 128 then not unique directly. O(1) space, O(1) time 

2. If the characters are only from a-z, then if the length is greater than 26, it is not unique. Can use an integer to store if the character has come previously or not. Basically int is 32 bits, so last 26 bit will shows the frequency of the character a-z. O(1) space, O(1) time.


*Implementation using hash, array and bit manipulation*
