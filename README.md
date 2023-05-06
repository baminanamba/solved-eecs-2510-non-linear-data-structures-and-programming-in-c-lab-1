Download Link: https://assignmentchef.com/product/solved-eecs-2510-non-linear-data-structures-and-programming-in-c-lab-1
<br>



For this programming lab, you are to implement the seven Dynamic Set Operators using a Binary Search Tree (BST).

The nodes for your tree will contain a string (the “key”), an integer (a piece of “Satellite data,” to count the number of times the string has been seen), and of course, left and right child pointers.  You may implement the parent pointer, if you think it will help you implement your solution, but it is not required.

Your program will consist of a loop within main, which will accept commands from the keyboard, and execute them one-at-a-time. The commands your program <strong><em><u>must</u></em></strong> support are:

<strong>insert</strong> &lt;string&gt;       If &lt;string&gt; is already IN the set, increment the count (stored in the nodecontaining &lt;string&gt;)

If &lt;string&gt; is NOT already in the set, add it to the set (and set the count to 1)

In either case, send &lt;string&gt; &lt;count&gt; to cout

<strong>delete</strong> &lt;string&gt;       If &lt;string&gt; is NOT in the set, output &lt;string&gt; &lt;-1&gt;.

If &lt;string&gt; IS in the set, and has a count of more than 1, decrement the count corresponding to the string, and output &lt;string&gt; &lt;nnn&gt;, where nnn is the new count

If &lt;string&gt; IS in the set, and has a count of exactly 1, delete it from the set,

and output &lt;string&gt; &lt;0&gt;

<strong>search</strong> &lt;string&gt;       If &lt;string&gt; is in the set, output &lt;string&gt; &lt;nnn&gt;, where &lt;nnn&gt; is the countfor the string.

If &lt;string&gt; is not in the set, output &lt;string&gt; &lt;0&gt;

<strong>min</strong>                             Output &lt;string&gt;, where &lt;string&gt; is the minimum value of the set.  If theset is empty, output a blank line

<strong>max</strong>                             Just like min, except output the maximum value of the set (or a blank line)

<strong>next</strong> &lt;string&gt;            If &lt;string&gt; is in the set, output its successor &lt;string&gt;.  If &lt;string&gt;doesn’t have a successor, or if it isn’t in the set, output a blank line

<strong>prev</strong> &lt;string&gt;            Just like <strong>next</strong>, except output the predecessor of &lt;string&gt;

<strong>list</strong>                           Does an in-order traversal, listing all of the strings in the tree in ascending order,along with the number of times each appears

<strong>help</strong>                           List the commands available to the user

<strong>exit</strong>                           Terminate the program




Note: the angle brackets shown above (&lt;&gt;) are not to be used for input or output; they’re shown only to indicate that a string &lt;string&gt; or a number (&lt;nnn&gt;) is to be input or output (see sample input/output below).

All of your lines of output should end in a new line (&lt;&lt; endl or “
”)

Your input <em><u>commands</u></em> should be case-<em><u>in</u></em>sensitive, but <em><u>not</u></em> the strings on which the commands operate (i.e., “cat” and “Cat” are two different strings, but “insert cat” and “InSeRt cat” would do the same thing).  The strings will be single words, so you don’t have to worry about parsing entire lines.




You should implement the BST as a class (perhaps called BST?), using an #include file for the interface, and a .cpp file for the implementation (see Savitch pp. 476-488).  If you implement the nodes as their own class (a struct will suffice, so you don’t have to), then you’ll need another .h/.cpp pair for that, too.

Some of you may have had occasion to code in C (or in “C-Style” C++) somewhere along the way.  You should NOT use the old-style C-Strings; rather, use the new standard string class (see chapter 9, Savitch).  The new class functions much more like Java’s String class, and in some ways is even more flexible (for example, you can use the == operator to compare the <em><u>contents</u></em> of two strings, rather than their <em><u>references</u></em>).

You already have snippets of code (in the lecture slides) for some of the operations you will need, and you have pseudocode for all of the set operators.  You may need to code some other methods, but the main ones should be rather straightforward.

All code you write for this assignment must be yours and yours alone (except for what is in the lecture slides and the Savitch text, of course).  You may <em><u>not</u></em> use any code from any other source, including the Internet, even as a reference.  Using code other than what you write (or are explicitly permitted to use) will be considered academic dishonesty, and will be dealt with in most severe terms.

Sample input and output:

<u>Input               </u>            <u>Output             </u>

search cat     cat 0

min            &lt;no output&gt;

max            &lt;no output&gt;

next cat       &lt;no output&gt;

insert cat     cat 1

insert cat     cat 2

search cat     cat 2

delete cat     cat 1

insert dog     dog 1

list           cat 1

dog 1

next cat       dog

prev dog       cat

Your program should utilize good programming practices – information hiding, etc.  Your public methods should not give away HOW the BST works – main() should never see your BST’s root pointer, for example.  You will have to create some public methods that, in turn, call private methods to get the job done.  Your “dynamic set” could just as easily be implemented with arrays, a linked list, or something else. What gives it its behavior is its interface; not its implementation!

Your code must be well-documented:

<ul>

 <li>Use block comments at the start of each method, briefly explaining <em>what</em> it does, and <em>how</em> it does what it does.</li>

 <li>Use line comments liberally to explain what’s going on</li>

 <li>Use internal documentation, like descriptive variable names where appropriate</li>

 <li>Make SURE you have a suitable block header on ALL of your source files WITH YOUR NAME!</li>

</ul>

Some helpful starting points:

<ul>

 <li>Create your program as a Win32 Console application within VS 2015</li>

 <li>Your program should use the std namespace; NOT the System namespace</li>

 <li>To get access to cin and cout, use “#include &lt;iostream&gt;”</li>

 <li>To get access to the string class and its supporting code, “#include &lt;string&gt;”</li>

</ul>




I strongly suggest your write this code incrementally.  You might want to start with just the command-soliciting loop.  Next build a shell of the BST class, and finally, implement and test the functionality one method at a time.

As for testing, you may want to create some test scripts, and store them in text files.  Assuming you called your program BST, then you can redirect input from a text file (from the command line) using the “&lt;” operator.  If TEST1.TXT contains a set of data you want to test your program against, then you can use BST &lt; TEST1.TXT to have the input that <em><u>would</u></em> have come from the keyboard come <em><u>instead</u></em> from TEST1.TXT


