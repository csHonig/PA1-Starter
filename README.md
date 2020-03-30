# Programming Assignment 1: C++ Review
In this Programming Assignment, you will be reviewing some principles of C++ to ensure that you are ready for the future (more involved) Programming Assignments and Projects.

## Part 1: Hello, World! (25 points)
In the world of programming, a ["Hello, World!" program](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program) is a simple computer program that generally does something simple such as output a short string of text (e.g. ``"Hello, World!"``) in order to test basic functionality of your environment.

### Task: Edit [``HelloWorld.cpp``](HelloWorld.cpp)
In this repository, there is a file called [``HelloWorld.cpp``](HelloWorld.cpp) that is currently essentially blank. In this part of the assignment, you will fill in the code in order to make a program that works as follows:
* It must first prompt the user with the message ``Enter name: ``
* Then, the user must type in their name and hit the ``ENTER`` key
* Then, the program must print the message ``Hello, <NAME>!`` on one line followed by ``Welcome to CSE 100!`` on the next line

We will compile your code as follows:

```bash
g++ -Wall -pedantic -O3 -o HelloWorld HelloWorld.cpp
```

Here's an example of how it should look when it's compiled and run from the command line (assuming I enter the name ``Niema``):

```
$ g++ -Wall -pedantic -O3 -o HelloWorld HelloWorld.cpp
$ ./HelloWorld
Enter name: Niema
Hello, Niema!
Welcome to CSE 100!
```

## Part 2: Swap (25 points)
In Java, we were unable to write methods to swap the values of two variables because everything in Java is **pass-by-value**: local variables inside of the method are *copies* of the variables that were passed in. In C++, however, we can take advantage of **pass-by-reference** to *finally* implement a swap function!

### Task: Edit [``Swap.cpp``](Swap.cpp)
In this repository, there is a file called [``Swap.cpp``](Swap.cpp) that is currently essentially blank. In this part of the assignment, you will fill in the code in order write a global function called ``swap`` that swaps the values of two ``int`` arguments. We have provided a tester program, [``SwapTest``](SwapTest.cpp), that will help you test your code. You can compile it as follows:

```bash
g++ -Wall -pedantic -O3 -o SwapTest SwapTest.cpp Swap.cpp
```

Here's an example of how it should look like when it's compiled and run from the command line (assuming I enter the numbers ``21`` and ``42``):

```
$ g++ -Wall -pedantic -O3 -o SwapTest SwapTest.cpp Swap.cpp
$ ./SwapTest
Enter first number: 21
Enter second number: 42
42 21
```

## Part 3: The Fast Saga (25 points)
Arguably one of the most amazing masterpieces of our time, the [Fast Saga](https://en.wikipedia.org/wiki/Fast_%26_Furious) is a series of movies that will have you yelling "Ejecto seato, cuz!" and living your life a quarter mile at a time. What started as a humble early-2000s film about street racing somehow evolved into the most ambitious cinematic universe in existence (that's right; step aside, [MCU](https://en.wikipedia.org/wiki/Marvel_Cinematic_Universe)). The only problem is that they keep churning out new entries in the [main series](https://en.wikipedia.org/wiki/Fast_%26_Furious#The_Fast_Saga), [spin-off movies](https://en.wikipedia.org/wiki/Fast_%26_Furious#Spin-off_films_2), and... even an [animated Netflix Original TV show](https://en.wikipedia.org/wiki/Fast_%26_Furious_Spy_Racers)?? When did that happen?? Regardless, the frequent releases and largely inconsistent naming schemes ([F9](https://en.wikipedia.org/wiki/F9_(film))? Seriously? How is anybody going to Google that?) make the Fast Saga pretty hard to keep track of. Fortunately for us, we're amazing programmers!

### Task: Edit [``FastSaga.cpp``](FastSaga.cpp)
In this repository, there is a file called [``FastSaga.cpp``](FastSaga.cpp) that contains the initial steps towards writing a custom ``FastSaga`` class to store the Fast Saga movie titles. It essentially wraps around a C++ [``vector``](http://www.cplusplus.com/reference/vector/vector/), with each movie title stored as a [``string``](http://www.cplusplus.com/reference/string/string/). We want to be able to iterate over the elements of a ``FastSaga`` object in-order using an [``iterator``](http://www.cplusplus.com/reference/iterator/) (e.g. using a [for-each](https://www.geeksforgeeks.org/g-fact-40-foreach-in-c-and-java/) loop). All that remains is that you need to fill in the ``begin()`` and ``end()`` functions. Note that you do *not* need to use a for-each loop (or any loop at all!) inside of these methods: implementing these two methods *allows* one to *iterate over* a ``FastSaga`` object using a for-each loop (as we do in the ``main()`` function of [``FastSagaTest.cpp``](FastSagaTest.cpp)).

We have provided a tester program, [``FastSagaTest``](FastSagaTest.cpp), that will help you test your code. You can compile it as follows:

```bash
g++ -Wall -pedantic -O3 -o FastSagaTest FastSagaTest.cpp FastSaga.cpp
```

Here's an example of how it should look like when it's compiled and run from the command line:

```
$ g++ -Wall -pedantic -O3 -o FastSagaTest FastSagaTest.cpp FastSaga.cpp
$ ./FastSagaTest
The Fast and the Furious
2 Fast 2 Furious
The Fast and the Furious: Tokyo Drift
Fast & Furious
Fast Five
Fast & Furious 6
Furious 7
The Fate of the Furious
Fast & Furious Presents: Hobbs & Shaw
F9
```

## Part 4: Implementing a Queue (25 points)
This course is an ***Advanced*** Data Structures course, meaning we anticipate that you already have prior experience implementing Data Structures and Abstract Data Types (ADTs). One such Data Structure with which we expect you to be familiar is the [Linked List](https://en.wikipedia.org/wiki/Linked_list), and one such ADT with which we expect you to be familiar is the [Queue](https://en.wikipedia.org/wiki/Queue_(abstract_data_type)).

### Task: Edit [``Queue.cpp``](Queue.cpp)
In this repository, there is a file called [``Queue.cpp``](Queue.cpp) that contains the initial steps towards writing a Queue ADT implementation using a Singly-Linked List. Function headers (with usage details) are included in [``Queue.h``](Queue.h), and you need to fill in the constructor, destructor, and all functions.

We have provided a tester program, [``QueueTest``](QueueTest.cpp), that will help you test your code. You can compile it as follows:

```bash
g++ -Wall -pedantic -O3 -o QueueTest QueueTest.cpp Queue.cpp
```

Here's an example of how it should look like when it's compiled and run from the command line:

```
$ g++ -Wall -pedantic -O3 -o QueueTest QueueTest.cpp Queue.cpp
$ ./QueueTest
Success
```

If it prints anything *other* than ``Success``, that means it has bugs. We expect you to be able to debug your code however you feel is best (e.g. print statements, ``gdb``, etc.). Remember that you will be dynamically creating ``Node`` objects, so beware of memory leaks!

## General Tips
We have provided a [``Makefile``](Makefile) to make compilation more convenient. Instead of having to type the ``g++ ...`` command each time you want to recompile your code, you can simply type ``make``. Here's an example of how it should look:

```
$ make
g++ -Wall -pedantic -O3 -std=c++11 -o HelloWorld HelloWorld.cpp
g++ -Wall -pedantic -O3 -std=c++11 -o SwapTest SwapTest.cpp Swap.cpp
g++ -Wall -pedantic -O3 -std=c++11 -o FastSagaTest FastSagaTest.cpp FastSaga.cpp
g++ -Wall -pedantic -O3 -std=c++11 -o QueueTest QueueTest.cpp Queue.cpp
```

If you want to clean up your environment by deleting all the compiled executables, you can simply type ``make clean``. Here's an example of how it should look:

```
$ make clean
rm -f HelloWorld SwapTest FastSagaTest QueueTest *.o
```

Feel free to [read more about what a ``Makefile`` does](https://www.geeksforgeeks.org/makefile-in-c-and-its-applications/) if you're curious!

## Academic Integrity
This Programming Assignment (PA) must be completed 100% independently! You may only discuss the PA with the Tutors, TAs, and Instructors. You are free to use resources from the internet, but you are not allowed to blatantly copy-and-paste code. If you ever find yourself highlighting a code snippet, copying, and pasting into your PA, you are likely violating the Academic Integrity Policy. If you have any concerns or doubts regarding what you are about to do, *please* be sure to post on Piazza first to ask us if it is okay.

## Grading (100 points total)
* **Part 1: Hello, World!**
    * 25 points for a correct solution
    * 0 points for an incorrect solution
* **Part 2: Swap**
    * 25 points for a correct solution
    * 0 points for an incorrect solution
* **Part 3: The Fast Saga**
    * 25 points for a correct solution
    * 0 points for an incorrect solution
* **Part 4: Implementing a Queue**
    * 25 points for a correct solution with no memory leaks
    * 15 points for a correct solution with memory leaks
    * 0 points for an incorrect solution

## Submission (Deadline: Tuesday, April 7, 2020 at 10:00 PM)
* Submit on [Gradescope](https://www.gradescope.com/)
* Late submissions **will not be accepted**
