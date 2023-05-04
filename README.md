Download Link: https://assignmentchef.com/product/solved-csci2500-homework-2-mips-assembly-code
<br>
<h2>Warm-Up Exercises (for Practice)</h2>

<ol>

 <li><strong>Textbook Problem 1.3</strong></li>

 <li><strong>Textbook Problem 1.5</strong></li>

 <li><strong>Textbook Problem 1.7</strong></li>

 <li><strong>Textbook Problem 1.13 (all sub-parts)</strong></li>

</ol>

<h2>Homework Problems</h2>

Use whatever software you like to write your answers to the textbook problems below. You must produce a PDF to submit for this assignment. Please name your PDF hw2.pdf. These will be manually graded by our TAs.

<ol>

 <li><strong>Textbook Problem 1.6</strong></li>

 <li><strong>Textbook Problem 1.9 (all sub-parts)</strong></li>

 <li><strong>Textbook Problem 1.12 (1.12.1 and 1.12.2 only)</strong></li>

 <li><strong>Textbook Problem 1.14 (all sub-parts)</strong></li>

</ol>

<h2>Coding Problem (to Submit for Credit)</h2>

Write a C program to take as input (via stdin) a valid assignment statement in C and generate MIPS assembly code to perform the given calculation(s). You can assume that each C variable name is one lowercase letter (e.g., a, b, c, etc.) and of type int. Further, positive int constants are also allowed as part of the given expression. For this assignment, you only need to support the addition (+) and subtraction (-) operators.

Note that you should use isspace(), islower(), isdigit(), scanf(), etc. to parse the input.

The MIPS code you generate must make use of registers $s0,$s1,…,$s7 to correspond to C variables and registers $t0,$t1,…$t9 to correspond to any temporary variables you need. Variables in MIPS should match those in C from left to right, meaning that the final result of the assignment statement must end up in register $s0.

You can assume that you will not need more than the specific MIPS registers listed here.

Below are a few example runs of your program. In the first example, register $s0 corresponds to C variable f, $s1 corresponds to g, and $s2 corresponds to h.

bash$ ./a.out

Please enter a valid C assignment statement:

f = g + h – 42;

The MIPS pseudocode is:

add $t0,$s1,$s2 sub $s0,$t0,42 bash$ ./a.out

Please enter a valid C assignment statement:

x = q – 12 + j;

The MIPS pseudocode is:

sub $t0,$s1,12 add $s0,$t0,$s2 bash$ ./a.out

Please enter a valid C assignment statement:

a = x – y + 13 + x – a;

The MIPS pseudocode is:

sub $t0,$s1,$s2 add $t1,$t0,13 add $t2,$t1,$s1 sub $s0,$t2,$s0

Be sure to match the above output formatting and ordering of operands exactly as shown (to ensure full credit on Submitty).

Note that if an error occurs, use either perror() or fprintf( stderr, “…” ), depending on whether the global errno is set.