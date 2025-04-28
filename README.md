# cs1501---algorithm-implementation---assignment-1-solved
**TO GET THIS SOLUTION VISIT:** [CS1501 – Algorithm Implementation – Assignment#1 Solved](https://www.ankitcodinghub.com/product/cs1501-algorithm-implementation-assignment11-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;56803&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS1501 – Algorithm Implementation – Assignment#1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (4 votes)    </div>
    </div>
<h1>OVERVIEW</h1>
<strong>Purpose:</strong>&nbsp; To implement backtracking algorithms and search trees.

<strong>Task 1: </strong>The first task of the assignment is to create a backtracking algorithm that finds <u>one</u> legal filling of the squares of a given crossword puzzle and the score of a filling (if a legal filling exists), as specified in detail below.

<strong>Task 2:</strong> The second task is to implement a De La Briandais (DLB) trie and use it to improve the search efficiency in Task 1 and hence to be able to produce a legal filling with <u>the highest score</u> of a given crossword puzzle.

<h1>BACKGROUND</h1>
Crossword puzzles are challenging games that test both our vocabularies and our reasoning skills.&nbsp; However, creating a legal crossword puzzle is not a trivial task.&nbsp; This is because the words both across and down must be legal, and the choice of a word in one direction restricts the possibilities of words in the other direction.&nbsp; This restriction progresses recursively, so that some word choices “early” in the board could make it impossible to complete the board successfully.&nbsp; For example, look at the simple crossword puzzle below (note: in this example X<sub>1</sub>, X<sub>2</sub>, X<sub>3</sub> are variables not the letter X):

&nbsp;

&nbsp;

&nbsp;

Assume that the word LENS has been selected for row 0 of the puzzle, as shown in Figure 1 above.&nbsp; Now, the word in column 1 (the second column) must begin with an E, the word in column 2 must being with an N and the word in column 3 must begin with an S. All single characters are valid words in our dictionary so the L in column 0 is a valid word but is also irrelevant to the rest of the puzzle, since its progress is blocked by a filled-in square.&nbsp; There are many ways to proceed from this point, and finding a

&nbsp;

<sup>1</sup> Assignment adapted from Dr. John Ramirez’s CS 1501 class.

good way is part of the assignment.&nbsp; However, if we are proceeding character by character in a row-wise fashion, we now need a letter X<sub>1</sub> such that EX<sub>1</sub> is a <em>valid prefix</em> to a word.&nbsp; Several letters will meet this criterion (EA, EB and EC are all valid prefixes, just to pick the first three letters of the alphabet).&nbsp; Once a possibility is selected, there are now two restrictions on the next character X<sub>2</sub>: NX<sub>2</sub> must be a valid word and X<sub>1</sub>X<sub>2</sub> must be a valid prefix to a word (see Figure 1). Assume that we choose Q for X<sub>1</sub> (since EQ is a valid prefix). We can then choose U for X<sub>2</sub>, (see Figure 2 (NU is a valid word in our dictionary)). Continuing in the same fashion, we can choose the other letters shown in Figure 2 (in our dictionary QUA, DU and DC are all legal words).

&nbsp;

Unfortunately, in row 3, column 1 we run into a problem (Figure 3).&nbsp; There is no word in our dictionary EQUX<sub>3</sub> for any letter X<sub>3</sub> (note that since we are at a terminating block, we are no longer just looking for a prefix) so we are stuck.&nbsp; At this point we need to undo some of our previous choices (i.e., backtrack) in order to move forward again toward a solution.&nbsp; If our algorithm were very intelligent, it would know that the problem that we need to fix is the prefix EQU in the second column<sup>2</sup>.&nbsp; However, based on the way we progressed in this example, we would simply go back to the previous square (row 3, column 0), try the next legal letter there, and move forward again.&nbsp; This would again fail at row 3, column 1, as shown in Figure 3.&nbsp; Note that the backtracking could occur many times for a given board, possibly going all the way back to the first word on more than one occasion.&nbsp; In fact, the general run-time complexity for this problem is <u>exponential</u>.&nbsp; However, if the board sizes are not too large, we can likely solve the problem (or determine that no solution exists) in a reasonable amount of time.&nbsp; One solution (but not the only one) to the puzzle above is shown in Figure 4.

<h1>FILLED PUZZLE SCORE</h1>
We are going to assign a score to each filled puzzle. The score is computed by adding up the letter points of all the letters on the filled puzzle. Assuming the letter points of the <a href="https://en.wikipedia.org/wiki/Scrabble_letter_distributions">Scrabble</a> game, the score of the puzzle of Figure 4 is computed as follows:

&nbsp;

L+E+N+S+T+O+N+A+C+O+T+H+A+W = 1+1+1+1+1+1+1+1+3+1+1+4+1+4=22

<h1>TASK 1 – FINDING A SINGLE SOLUTION</h1>
&nbsp;

The first task of your assignment is to create a legal crossword puzzle (if it exists) and compute its score in the following way:

1)&nbsp;&nbsp;&nbsp; Read a dictionary of words in from a file and form a MyDictionary object of these words. The name of the dictionary file should be specified as a command-line argument. The interface DictInterface (in DictInterface.java) and the class MyDictionary (in MyDictionary.java) are provided for you on Canvas, and you <strong>must</strong> use them in this assignment.&nbsp; Read over the code and comments carefully so that you understand what they do and how.&nbsp; The interface DictInterface will also be important for the second task of this assignment.&nbsp; The file used to initialize the MyDictionary will contain ASCII strings, one word per line.&nbsp; Use the file dict8.txt on Canvas.&nbsp; If you are unsure of how to use DictInterface and

&nbsp;

<sup>2</sup> It is actually possible to avoid selecting U for row 1, column 1 because there is no 4-letter word that starts with EQ in our dictionary. This is called pruning.

MyDictionary correctly, see the DictTest.java example program (and read the comments). Lab 1 solution can be used for reference as well.

&nbsp;

<ul>
<li>Read a crossword board in from a file. The name of the board file should be specified as a command-line argument.&nbsp; The crossword board will be formatted in the following way:</li>
</ul>
&nbsp;

<ol>
<li>The first line contains a single integer, N. This represents the number of rows and columns that will be in the board.&nbsp; Since the dictionary will contain up to 8-letter words, your program should handle crosswords up to 8×8 in size.</li>
</ol>
&nbsp;

<ol>
<li>The next N lines will each have N characters, representing the NxN total locations on the board.</li>
</ol>
Each character will be either

<ol>
<li>+ (plus) which means that any letter can go in this square</li>
<li>– (minus) which means that the square is solid (filled-in) and no letter can go in here</li>
</ol>
<ul>
<li>.Z (a letter from A to Z) which means that the specified letter must be in this square (i.e., the square can be used in the puzzle, but only for the letter indicated)</li>
</ul>
For the board shown above, the board file sample.txt is as follows: 4

++++

-+++

++-+

++++

&nbsp;

Some test boards have been put onto the assignment page on Canvas. <strong>Please consult testFiles.html for an overview of these board files. </strong>

&nbsp;

<ul>
<li>Create a legal crossword puzzle for the given board and print it out to standard output. Many of the test files may have many solutions, but for this part of the project you only need to find <strong>one solution</strong>.&nbsp; See the second task of this assignment for information about finding and comparing multiple solutions.&nbsp; For example, one output to the crossword shown above in Figure 4 would be (note that the puzzle score is also printed):</li>
</ul>
&nbsp;

&gt; java Crossword dict8.txt sample.txt

LENS

-TON

AC-O

THAW

Score: 22

&gt;

&nbsp;

Depending upon your algorithm, the single solution that you find may differ from that of my program or your classmates’ programs.&nbsp; This is fine as long as all of the solutions are legal.&nbsp; Note that because of the severe performance limitations of the MyDictionary class, some of the run-times for the test files will be very long.&nbsp; See more details on this in testFiles.html.

&nbsp;

<strong>Important Notes for Task 1: </strong>

&nbsp;

<table width="601">
<tbody>
<tr>
<td width="24">−</td>
<td colspan="2" width="577">For consistency, <strong>you must name your main program Crossword.java</strong>.</td>
</tr>
<tr>
<td width="24">−</td>
<td colspan="2" width="577">When grading your assignments, your TAs may redirect your output to a file so that they can refer to it at a later point.&nbsp; To make sure this will work correctly, make sure that once your search algorithm begins there is NO INPUT or anything that would make your program require any user interaction (since the TA will not see any prompts given that they will be sent to a file rather than the display).</td>
</tr>
<tr>
<td width="24">−</td>
<td colspan="2" width="577">To help you to get started,</td>
</tr>
<tr>
<td width="24"></td>
<td width="48">o</td>
<td width="529">first think of boards with all squares open (you can consider filled in squares later). In this case a solution for a KxK board will consist of K words of length K in the columns of the board and K words of length K in the rows of the board.</td>
</tr>
<tr>
<td width="24"></td>
<td width="48">o</td>
<td width="529">Your program has to make one <strong>decision</strong> for each square of the board. How many options do you have for each decision? What are these options? You will have to choose from the 26 letters.</td>
</tr>
<tr>
<td width="24"></td>
<td width="48">o</td>
<td width="529">Construct an array of K StringBuilders for the columns (call it colStr) and an array of K StringBuilders for the rows (call it rowStr), each initially empty. Now consider a single recursive call at square (i,j) on the board. For an option (i.e., a letter) at position (i,j) to be <strong>valid</strong>, the following must be true:

If j is not an end index, then rowStr[i] + the letter a must be a valid prefix in the dictionary

If j is an end index, then rowStr[i] + the letter must be a valid word in the dictionary

If i is not an end index, then colStr[j] + the letter must be a valid prefix in the dictionary

If i is an end index, then colStr[j] + the letter must be a valid word in the dictionary
</td>
</tr>
<tr>
<td width="24"></td>
<td width="48">o</td>
<td width="529">If the letter is valid, you append it to both corresponding StringBuilders and recurse to the next square (unless you are on the last square of the board, in which case you have a solution!). If it is not valid you try the next character at that square or, if all have been tried, you backtrack. <strong>Refer to the backtracking template that we discussed in the first recitation. </strong></td>
</tr>
<tr>
<td width="24">−</td>
<td colspan="2" width="577"><strong>Search algorithm details:</strong> Carefully consider the algorithm to fill the words into the board.&nbsp; Make sure it potentially considers all possibilities yet does not waste time rechecking prefixes that have already been checked.&nbsp;&nbsp; Although you are not required to use the exact algorithm described above, your algorithm must be a recursive backtracking algorithm that uses <strong><u>pruning</u></strong>.&nbsp; The algorithm you use can vary greatly in its efficiency.&nbsp; If your algorithm is very inefficient or otherwise poorly implemented, you will lose some style points.&nbsp; This algorithm is a significant part of the overall assignment, so put a good amount of effort into doing it correctly.&nbsp; <strong>For guidance on your board-filling algorithm, it is strongly recommended that you revise the Boggle game lab code. </strong></td>
</tr>
<tr>
<td width="24">−</td>
<td colspan="2" width="577">The MyDictionary implementation of the DictInterface that is provided to you should work correctly, but it is not very efficient.&nbsp; Note that it is doing a linear search of an ArrayList to</td>
</tr>
</tbody>
</table>
determine if the argument is a prefix or word in the dictionary.&nbsp; In the second task of this assignment you will write a more efficient implementation of the DictInterface.

− Be sure to thoroughly document your code, especially the code that fills the board.

<h1>TASK 2 – FINDING A HIGHEST-SCORE SOLUTION USING A DE LA BRIANDAIS (DLB) TRIE</h1>
In Task 1 of this assignment, you were asked to complete a recursive, backtracking solution to filling in the squares of a crossword puzzle.&nbsp; To do this you utilized the DictInterface interface and the MyDictionary class, both of which were provided for you.&nbsp; Unfortunately, the MyDictionary class implements the DictInterface in a somewhat primitive and inefficient way, utilizing a linear search of the dictionary array.&nbsp; This can lead to long run-times when many searches are required (as in the crossword problem!).

Consider the De La Briandais (DLB) tries, which we discussed in lecture and recitation.&nbsp; Since these tries allow a string to be tested as a word or as a prefix in the dictionary in (typically) time proportional to the length of the string, they appear to be a superior way to implement the DictInterface interface.&nbsp; In Task 2 of this assignment you will do the following:

<ul>
<li>Implement a DLB as a class, as discussed in lecture and in recitation. This requires the “nodes” within the DLB to contain a character field, a child reference and a sibling reference. Your class(es) should be written in reasonably good object-oriented style.&nbsp; You may have a number of methods in your DLB class, but it must minimally implement the DictInterface as specified.&nbsp; Verify that this implementation works by testing your DLB using the DictTest.java program that is provided for you on Canvas.</li>
<li>Modify your main program from Task 1 in the following ways:
<ol>
<li>Have the type of the DictInterface object as a command-line argument so that the user can run the same program with either a MyDictionary or a DLB. Look over DictTest.java to see how this would be done.</li>
<li>Update your program so that if the DictInterface object is a DLB it will find <strong>a HIGHESTSCORE solution</strong> rather than just the first solution. This can be done with two simple changes to your main program:
<ol>
<li>When a solution is found, test again to see the type of the DictInterface object. If the type is MyDictionary, stop the program execution, but if the type is DLB, compute the solution score, compare it with the highest-score so far, take appropriate action based on the comparison result, and continue execution.</li>
<li>Rather than having your backtracking algorithm complete (terminate) once a solution is found, have it backtrack and continue to search for solutions. This is the approach taken in the BoggleSolver.java program in Lab 1.&nbsp; Look over that to get an idea of how to do this.</li>
</ol>
</li>
</ol>
</li>
</ul>
At the end of your execution, print out a highest-score solution and the highest score that your program was able to find.&nbsp; <em>Don’t forget to do this as it will be used in evaluating the correctness of your algorithm.</em>

<ul>
<li>Compare the execution of your crossword solution with the MyDictionary to that using the DLB. Do this by informally recording the amount of time required for the first solution to be found (or for the program to terminate if no solutions exist) with both dictionaries.&nbsp; To informally time the programs, run them while watching your clock/watch/etc.&nbsp; We are not worried about exact times here – just</li>
</ul>
orders of magnitude.&nbsp; Based on your comparisons of the various test files, determine if there is a significant difference in the run-times.

<ul>
<li>For some test files, one or perhaps both versions will take several minutes or perhaps hours or even days. Based on some worst-case analysis and some real timing of the smaller files you should be able to get an idea of how long the larger files will take to run.&nbsp; If a program takes more than a few hours you can abort the execution.</li>
<li>Once you have completed your comparison runs, write a short paper (2-3 pages, double-spaced) that summarizes your project in the following ways:</li>
</ul>
<ol>
<li>Discuss how you solved the crossword-filling problem in some detail. Include
<ol>
<li>how you set up the data structures necessary for the problem and</li>
<li>how your algorithm proceeded.</li>
</ol>
</li>
</ol>
<ul>
<li>Also indicate any coding or debugging issues you faced and how you resolved them. If you were not able to get the program to work correctly, still include your approach and speculate as to what still needs to be corrected.</li>
</ul>
<ol>
<li>Discuss the differences (if any) between the run-times of the program using the</li>
</ol>
MyDictionary and the program using the DLB.&nbsp; Include the (approximate) run-times for the programs for the various files <strong>in a table</strong>.

<ol>
<li>Include an asymptotic analysis of the worst-case run-time for each version of the program.</li>
</ol>
Some values to consider in this analysis may include:

<ol>
<li>Number of words in the dictionary</li>
<li>Number of characters in a word</li>
</ol>
<ul>
<li>Number of possible letters in a crossword location iv. Number of crossword locations in the puzzle</li>
</ul>
If you were unable to complete the crossword solving program, speculate (using some intelligent guessing) for the actual run-times, but still include the comparison in your paper.

<strong>Important Notes for Task 2: </strong>

<ol>
<li>For consistency in grading and testing, you must call your main program CrosswordB.java and your DLB class DLB and it must be in a file named DLB.java.</li>
<li>When grading your assignments, your TAs may redirect your output to a file so that they can refer to it at a later point. To make sure this will work correctly, make sure that once your search algorithm begins there is NO INPUT or anything that would make your program require any user interaction (since the TA will not see any prompts given that they will be sent to a file rather than the display).</li>
<li>Read over the test file page testFiles.html on Canvas for important information on the test files and some expected results.</li>
<li>Be sure to thoroughly document your code.</li>
<li>This assignment was devised so that Task 1 and Task 2 could be implemented independently. If you are unable to complete one task don’t let that prevent you from completing the other.&nbsp; Also, be sure to try each and submit something so that you can get some partial credit.</li>
</ol>
<h1>EXTRA CREDIT</h1>
If you are interested in some extra credit for this assignment, here are some possibilities:

<ol>
<li>Create a third implementation of the DictInterface and compare its performance to that of the other two implementations. One possibility is to use binary search of a sorted array.&nbsp; However, searching for a prefix is tricky if binary search is used, so be careful with this approach (i.e., make sure it is correct).</li>
<li>Do more detailed analysis of the run-times of the two different DictInterface implementations. Add timing to your program and do multiple runs to obtain (reasonably) accurate values of the actual run-times. Create a graph to show how the run-times increase as the crossword board size increases.</li>
<li>Add and demonstrate (through a driver program that you write yourself) a delete() method for your DLB.</li>
</ol>
<h1>SUBMISSION REQUIREMENTS</h1>
You must submit the following files <strong>individually</strong> to GradeScope:

<ul>
<li>java</li>
<li>java</li>
<li>java</li>
<li>Any other helper files that you had to add to support your implementation</li>
<li>Well written/formatted paper explaining your search algorithm and results (see Task 2 above for details on the paper)</li>
<li>Assignment Information Sheet (including compilation and execution information).</li>
</ul>
<table width="720">
<tbody>
<tr>
<td width="375"><strong>De La Briandais Tree Implementation: </strong></td>
<td width="345"></td>
</tr>
<tr>
<td width="375">DLB implemented as a class that implements DictInterface:</td>
<td width="345">10</td>
</tr>
<tr>
<td width="375">DLB node structure is correct:</td>
<td width="345">10</td>
</tr>
</tbody>
</table>
The idea from your submission is that your TA can compile and run your programs <strong>from the command line</strong> WITHOUT ANY additional files or changes, so be sure to test it thoroughly before submitting it. If the TA cannot compile or run your submitted code it will be graded as if the program does not work.

If you cannot get the programs working as given, clearly indicate any changes you made and clearly indicate why on your <u>Assignment Information Sheet</u>.&nbsp; You will lose some credit for not getting it to work properly, but getting the main programs to work with modifications is better than not getting them to work at all.&nbsp; A template for the Assignment Information Sheet can be found in the assignment’s CourseWeb folder. You do not have to use this template, but your sheet should contain the same information.

<strong><u>Note: If you use an IDE, such as NetBeans, Eclipse, or IntelliJ, to develop your programs,</u></strong><strong> <u>make sure the programs will compile and run on the command-line before submitting –</u> <u>this may require some modifications to your program (e.g., removing package</u> <u>information).</u></strong>

<h1>RUBRICS<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a></h1>
&nbsp;

&nbsp;

<table width="720">
<tbody>
<tr>
<td width="375">DLB add method works correctly</td>
<td width="345">15</td>
</tr>
<tr>
<td width="375">DLB searchPrefix method works correctly</td>
<td width="345">15</td>
</tr>
<tr>
<td width="375"><strong>Crossword Puzzle Search </strong></td>
<td width="345"></td>
</tr>
<tr>
<td width="375">Basic search approach is correct:</td>
<td width="345">10</td>
</tr>
<tr>
<td width="375">Search works for board with all open squares:</td>
<td width="345">20</td>
</tr>
<tr>
<td width="375">Search works for board with filled in squares:</td>
<td width="345">10</td>
</tr>
<tr>
<td width="375">Highest-score solution found in DLB version:</td>
<td width="345">10</td>
</tr>
<tr>
<td width="375">Algorithm works in an efficient manner:</td>
<td width="345">10</td>
</tr>
<tr>
<td width="375"><strong>Main Program and Other Requirements: </strong></td>
<td width="345"></td>
</tr>
<tr>
<td width="375">Dictionary file read in/processed correctly:</td>
<td width="345">5</td>
</tr>
<tr>
<td width="375">Crossword file read in/processed correctly:</td>
<td width="345">5</td>
</tr>
<tr>
<td width="375">Output generated / formatted correctly:</td>
<td width="345">10</td>
</tr>
<tr>
<td width="375">Write-up paper:</td>
<td width="345">10</td>
</tr>
<tr>
<td width="375">Code style and documentation</td>
<td width="345">10</td>
</tr>
<tr>
<td width="375">Assignment Information Sheet</td>
<td width="345">5</td>
</tr>
<tr>
<td width="375"><strong>Extra Credit </strong></td>
<td width="345"></td>
</tr>
<tr>
<td width="375">Third implementation of DictInterface</td>
<td width="345">8</td>
</tr>
<tr>
<td width="375">More detailed run-time measurements</td>
<td width="345">5</td>
</tr>
<tr>
<td width="375">DLB delete</td>
<td width="345">7</td>
</tr>
</tbody>
</table>
&nbsp;

<a href="#_ftnref1" name="_ftn1">[1]</a> The definitive version of the rubrics is on Gradecope.
