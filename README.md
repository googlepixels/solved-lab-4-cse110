Download Link: https://assignmentchef.com/product/solved-lab-4-cse110
<br>
<em>Topics</em>

<ul>

 <li>Using conditional (if, if-else) statements – Chapter 3</li>

 <li>Using loops – Chapter 4</li>

</ul>

<em>Coding Guidelines</em>

<ul>

 <li>Give identifiers semantic meaning and make them easy to read (examples numStudents, grossPay, etc).</li>

 <li>Keep identifiers to a reasonably short length.</li>

 <li>Use upper case for constants. Use title case (first letter is upper case) for classes. Use lower case with uppercase word separators for all other identifiers (variables, methods, objects).</li>

 <li>Use tabs or spaces to indent code within blocks (code surrounded by braces). This includes classes, methods, and code associated with ifs, switches and loops. Be consistent with the number of spaces or tabs that you use to indent.</li>

 <li>Use white space to make your program more readable.</li>

 <li>Use comments after the ending brace of classes, methods, and blocks to identify to which block it belongs.</li>

</ul>

<em>Assignment/Lab Documentation</em>

At the beginning of each programming assignment you must have a comment block with the following information:

/*————————————————————————-

// AUTHOR: your name

// FILENAME: title of the source file

// SPECIFICATION: description of the program

// FOR: CSE 110- Lab #4

// TIME SPENT: how long it took you to complete the assignment

//———————————————————–*/

<em>Getting Started</em>

Create a class called Lab4. Use the same setup for setting up your class and main method as you did for the previous assignments. Be sure to name your file Lab4.java.

<em>Hints</em>

<ul>

 <li>Example of using a loop to read in sentinel values can be found in Section 4.5 of the book as well as the example videos for the week. The instructions below follow the example in the sample video.</li>

 <li>Examples of loops for various tasks can be found in Section 4.7 of the book as well as the videos for the week.</li>

</ul>

<em>Part 0: Task Overview</em>

The overall goal of this lab is to continually read in integers, one at a time, from the user until a 0 is entered. 0 should not be counted as an input, but rather is a sentinel used to stop the loop. At this point, if the user entered any values (besides 0) the following output should be displayed:

<ul>

 <li>A line stating the smallest integer the user entered</li>

 <li>A line stating the largest integer the user entered</li>

 <li>A line stating the number of integers entered</li>

 <li>A line stating the number of even integers entered</li>

 <li>A line stating the number of odd integers entered</li>

 <li>A line stating the average value of all of the integers that the users entered</li>

</ul>

Otherwise a warning message should be displayed. <em>IMPORTANT: Please do not include the 0 in these calculations! </em>The basic outline for the code logic is given below:

<em>Part 1: Before the while</em>

These steps should be carried out in your main method prior to starting the while loop.

<ol>

 <li>Set up the Scanner.</li>

 <li>Declare and initialize variables needed for the calculations in the loop.

  <ul>

   <li>Note: It is important to declare these before the loop since they need to be printed out after the loop. Any variable declared in the loop is only usable inside of the loop.</li>

   <li>The following variables will be needed (You can see the coding sample video with sentinel values and averages for an example of initializing a couple variables before a loop. Here we just initialize more):

    <ul>

     <li>largest number (see below about initializing these)</li>

     <li>smallest number (see below about initializing these)</li>

     <li>a counter for how many integers have been entered (this would be initialized to 0, since before the loop no integers have been entered yet)</li>

     <li>number of even integers (how many have been entered before the loop is started?)</li>

     <li>number of odd integers (how many have been entered before the loop is started?)</li>

     <li>sum of all the values entered needed for the average (what is the sum before any value is entered?)</li>

     <li>a variable to hold the input. Prompt the user to “Enter a series of values (0 to quit):”</li>

    </ul></li>

  </ul></li>

</ol>

<ol start="4">

 <li>Read in the first value with the Scanner and store this in the variable used to hold the input.</li>

 <li>Initialize the variable that holds the largest and smallest values to the first input just read in.</li>

</ol>

<ul>

 <li>Note: These must be initialized to the first value entered to work properly. If they were just initialized to 0 then if the user never entered any negative numbers, the minimum would remain</li>

</ul>

<ol>

 <li>Similarly, if the user never entered any positive numbers, the maximum would remain 0.</li>

</ol>

<em>Part 2: Setting up the while</em>

Now we are ready for the loop.

<ul>

 <li>Set up a while loop to continue while the input is not equal to 0, the sentinel value.</li>

 <li>For this sentinel problem we will use a while loop (though other loops could be used, particularly the do while with an extra if).</li>

 <li>We will have multiple statements inside the while loop. These must go in braces. For example:</li>

</ul>

while (input not equal to 0) {

// Put the instructions below in here }

<em>Part 3: Inside the while loop</em>

This is where we will calculate all the needed values. The order these are done inside the loop is not important. You should add these one at a time and check to make sure the result is working correctly before adding more.

<ol>

 <li>First find the maximum and minimum values.

  <ul>

   <li>The idea is given in the if statements in the while loops in Section 4.7.5. For the maximum (the minimum can be found with a small change):</li>

  </ul></li>

</ol>

if (input greater than maximum) maximum = input // update max

<ol start="2">

 <li>Find the number of even integers entered.

  <ul>

   <li>To find if the current input value is even or odd you can use the remainder operator with 2 (input % 2). If the result is 0, the number is even. Otherwise it is odd. The logic for this part then is:</li>

  </ul></li>

</ol>

if (input is even) // that is input % 2 is 0 increase number of evens by 1 otherwise increase number of odds by 1

<ol start="3">

 <li>Calculate the updated sum.

  <ul>

   <li>Add the current input to the sum and save the result back in the sum. You can get an idea from section 4.7.1 or the sentinel average program example.</li>

  </ul></li>

 <li>Increase the counter by one since one more input has been seen.

  <ul>

   <li>This is as done in the Average example in section 4.7.1 or the sample video with the counter line.</li>

  </ul></li>

 <li>Finally, read in the next input value.

  <ul>

   <li>This updates the loop control variable to be ready to process the next input.</li>

  </ul></li>

</ol>

<em>Part 4: After the Loop</em>

This section goes after the close brace ’}’ of the while loop. Here we will print the results if any data has been entered or print a message that “No data was entered”. The Average example in 4.7.1 and the Sentinel Average video sample show checking to make sure input was entered.

<ol>

 <li>If any data has been entered (What would the count be if only 0 was entered?)

  <ul>

   <li>Print out the results stating the max, min, number of integers entered, number even and odd.</li>

  </ul></li>

</ol>

(See sample output below)

<ul>

 <li>Calculate the average, by dividing the sum by the count and display the results. Be careful of integer division if both the sum and count are integer variables.</li>

</ul>

<ol start="2">

 <li>Otherwise, only the sentinel was entered, so output a warning that “No data was entered”.</li>

</ol>

<em>Sample Output</em>

Below is an example of what your output should roughly look like when this lab is completed. All text in bold represents user input.

Sample Run 1:

Enter a series of integers (zero to quit):

<strong>3</strong>

<strong>-4</strong>

<strong>5</strong>

<strong>12</strong>

<h1><a name="_Toc536215069"></a><strong>-7 0</strong></h1>

<h1><a name="_Toc536215070"></a>The smallest integer is -7</h1>

<h1><a name="_Toc536215071"></a>The largest integer is 12</h1>

<h1><a name="_Toc536215072"></a>Total number of integers entered is 5</h1>

Total even numbers entered is 2

Total odd numbers entered is 3

The average value is 1.8

Sample Run 2:

Enter a series of integers (zero to quit):

<strong>-10</strong>

<a href="#_Toc536215069"><strong>-7 0</strong>   4</a>

<a href="#_Toc536215070">The smallest integer is -7  4</a>

<a href="#_Toc536215071">The largest integer is 12  4</a>

<a href="#_Toc536215072">Total number of integers entered is 5  4</a>


