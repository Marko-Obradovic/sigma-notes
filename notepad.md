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



chris' exhibitions tool:
https://exhibitions.london/

How to solve any problem:
(location of svg in images)
![[Pasted image 20250111065440.png]]


positional/named arguments - FIND MORE ABOUT THIS AND THE FLIP SIDE

syntaxErrors, TypeErrors, etc -> Crashed
	These are good, you can see what's happened and it doesn't let you move on until you've fixed them.

Logical Error -> Did something wrong
	
LOOK INTO ERRORS MORE


look into graceful degredation

today we learned oop and error handling


look into Encapsulation vs abstraction 




NEW:
What I'm looking for in my career now is an opportunity to deepen my technical skills in data engineering and contribute to an impactful project in a highly collaborative environment. 
I'm extremely eager to work in an environment where I can learn from experts in their field, work with complex datasets and help solve solutions to real world problems through code. I admire Apple's strong focus on innovating, constantly building and improving the current data infrastructure; this perfectly aligns with my recent experiences and my passion for optimising systems and creating scalable solutions.
I am particularly inspired by Apple's cross-functional collaboration; you can see this in all of Apple's products and the way they integrate seamlessly. Working in such a dynamic and collaborative environment is a dream of mine; somewhere that foster innovation and gets the best out of everyone on the team.


- Their company mission and values
	a story of growth, purpose, and transformation, emphasising Virgin Media Business as a key player in enabling digital innovation and connectivity across the UK and beyond.
		
		- Supporting Education through initiatives like Generation Tech
		- showing a big focus on sustainability
		- 

	- meaningful collaboration
		- key partnerships with EE, Three, Sky?,  and the UK government reflect its ability to work collaboratively to create impactful solutions


the company demonstrates a commitment to innovation, providing state of the art infrastructure and focusing on what matters. I was always inspired by when people come together and use technology to create high quality solutions to big issues.
- big red internet 2010 - the first dedicated leased line service that gives people all the bandwidth they need, without restrictions or extra charges
- Often extending and improving Public Service Network security
- Investing £3bn into enhancing broadband conectivity through Project Lightning

Virgin does this in ways which is both sustainable and empowers others, which shows that they put a lot of thought into every step they take.
	• Fostering decent work and economic growth
		- Create a supportive, inclusive workplace
		- Prioritise wellbeing and mental health
		- Empowers all colleagues, including unpaid carers.  
	• Promote ways to make more sustainable choices. 
		- Reusing or Recycling all returned customer equipment
		- Zero single use packaging and all packaging to be 100% recyclable.  
	• Encourage community participation and building safe, inclusive and accessible community spaces across UK neighbourhoods.

I especially hold a lot of respect for Virgin's 2014 education initiative, Generation Tech; educating kids in technology is incredibly important for all our futures, and it's great to see a large-scale company go out of its way to do this.



overthink problems before starting
try to solve multiple problems at once, thinking its all one problem

trying to solve by:
- putting an emphasis on breaking down problems into their most relevant components
- working chronologically
- not worrying about what the next steps are until finishing the one I'm on

so far I have noticed:
- I'm working through problems more methodically
- getting faster
- seeing how everything fits in the bigger picture






What are the differences between consoles, terminals, CLI, and shells?
	- Console: Was referred to a physical device that's used to directly interact with old mainframes - now it refers to theterminal environment that allows you to interact directly with the system.
	- terminal: The software that allows you to run commands for your shell to interpret and return information. The terminal is what shows you the returns.
	- CLI (Command Line Interface): A text-based interface for interacting with a system.
	- Shell: A program that runs in the terminal. The shell is what interprets commands you enter into the terminal. It will parse the command, execute it and display the output via the terminal.
	  Examples: Bash, Zsh, PowerShell
	
What do the terms 'flag', 'option' and 'argument' mean when discussing command-line tools?
	Flag: type of option that doesn't take a value. Only acts as a boolean switch. They are short and consist of single letters, prefixed with a dash. E.g -v stands for verbose, activating detailed output
	Option: Argument that modifies the behavior of the command. Can be followed by a value or flag. Options are generally prefixed with one or more dashes such as -h or --help.
	Argument: Values that follow the command and options. Things like files, directories, URLs etc.


What is the Python library argparse used for?
	argparse is used for creating command-line interfaces - it allows you to define what arguments your program expects, parse those arguments, and then use them within the program. With this, you can define options, flags, and positional arguments for your command-line tool. It also handles help messages and error checking.

What curl command would you use to access the data at this link and store it in a file called TSCDJMH.txt?
curl -o TSCDJMH.txt https://www.gutenberg.org/files/43/43-0.txt

How many words, lines, and characters are there in TSCDJMH.txt?
2556 lines, 25647 words, 143715 characters

How many times does the word 'scientific' appear in TSCDJMH.txt
6 times

