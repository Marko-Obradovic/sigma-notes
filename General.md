Quickly jot down notes here and consolidate them + add to their respective files later.

 no type hints

no if __name__ == main

functions, variables and parameters are badly named and unclear (gen_wor, wlist, i)

no docstrings


constant variables should ALWAYS be global, never in a function

bring up the const global variables breaking SoC

KEY TAKEAWAYS:
type hints
no magic numbers
good variable names


we're writing procedural code
- no rigid structure to it

other types:
OOP

functional programming


map function in python:


lay out steps: 
write code that works
clean code (good abstraction)
its tested
its performant (fast)




gonna use dictionaries for first assessment


1. read traceback
2. find the line
3. come up with a theory
4. implement
5. if it works, move on
6. if it doesn't, UNDO what you did and go back to 3

if you don't get an error:
first go to google, then slackbot then questions

what does larger scale software development look like:
[https://www.youtube.com/watch?v=Dl-BdxNRUqs](https://www.youtube.com/watch?v=Dl-BdxNRUqs)

pework:

the code takes in a phone number that, if correct, will be formatted and printed in the correct format.

Bug 1: 
1. 'is' should be == in is_number_valid_length() and is_UK_number(). 'is' is checking for if both are pointing to the same object location, which they aren't. == will compare values, which will give True if the values are equal.
2. If the bug was corrected, True would be passed when the values are equal and convert_phone_to_UK_Format() would get accurate inputs.
3. The bug makes it so that you get False from 'is' instead of the expected True if the values are the same.
Bug 2:
1. .contains() in main() is not a method, you should be checking if something is in a list using using 'in'
2. If the code was corrected, it would be giving a the correct bool based on whether the values are in the list.
3. The bug gives you an error stating that .contains() doesn't exist.
![[Pasted image 20250111064127.png]]
cracking the coding interview

for performance and algorithms:
[https://www.crackingthecodinginterview.com/](https://www.crackingthecodinginterview.com/)

automatic notes with ai:
[https://www.limitless.ai/](https://www.limitless.ai/)

chris' exhibitions tool:
https://exhibitions.london/

How to solve any problem:
(location of svg in images)
![[Pasted image 20250111065440.png]]