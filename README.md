Download Link: https://assignmentchef.com/product/solved-comp1210-activity7-arrays
<br>
By the end of this activity you should be able to do the following:

Ø Understand the basics of instantiating arrays and assigning / accessing array elements. Ø How to iterate through arrays using loops.

<strong>Description: </strong>

In this activity, you will create a class called Scores that will hold an array of numerical values and provide methods that allow users to interact with the Scores class.

<strong>Directions: </strong>

<u>Don’t forget to add your Javadoc comments for your classes, constructor, and methods in this activity</u>.<strong> Part 1: Scores – instance variable, constructor and method stubs  </strong>•         Create a class called Scores.  o Add an instance variable with the name numbers to your class that is an array of int values:

o Add a constructor that has a parameter declared as an array of int values.

<ul>

 <li>Add <u>method stubs</u> for the following methods<strong>. The first one is given; do the rest on your own</strong>.</li>

 <li>findEvens: no parameter, returns an array of int (all of the even-valued scores)</li>

</ul>

<sub>             </sub> o findOdds: no parameter, returns an array of ints (all of the odd-valued scores) o calculateAverage: no parameters; returns a double (the average of all scores) o toString: no parameters; returns a String containing all scores

<ul>

 <li>toStringInReverse: no parameters; returns a String containing all scores in reverse order</li>

</ul>

Compile Scores and run the following in interactions. <strong>Do not continue until your program compiles and the following code runs without error in interactions. </strong>

Ï¼ÏÏScores s = <strong>new</strong> Scores(<strong>null</strong>);

Ï¼ÏÏ<strong>int</strong>[] evens = s.findEvens();

Ï¼ÏÏ<strong>int</strong>[] odds = s.findOdds();

Ï¼ÏÏ<strong>double</strong> avg = s.calculateAverage();<strong>            </strong>

<strong>Part 2: Scores – completing the constructor </strong>

<ul>

 <li>In your constructor, add code that will set the value of numbersIn to numbers. <strong>You access the entire array object using its variable name with no brackets.</strong></li>

 <li>Compile Scores. In the interactions pane set up an array of int values using an initializer list and send it to the constructor of scores:</li>

</ul>

Ï¼ÏÏ<strong>int</strong> [] nums = {2, 5, 8};

Ï¼ÏÏScores s = <strong>new</strong> Scores(nums);




On the Workbench tab, click the Open New Viewer Canvas button , then drag the array nums and the Scores object s from the Workbench tab onto the canvas window.  You should now be able to see the values of each of these items. To change the viewer for a variable on the canvas, select the viewer for the variable, then click the viewer menu button  (at upper right of viewer frame), select “Viewer”, then select the desired viewer from the list.  You should experiment with different viewers. Below, the “Presentaton – Structure Identifier” viewer has been selected for nums and the “Basic” viewer has been selected for variable s.  You should leave the canvas window open for the remainder of the activity since we will be adding other variables.







<strong>Canvas with int array <em>nums</em> and Scores <em>s</em> </strong>

Change the values in the int array nums using assignment statements in interactions as indicated below and you should see the viewer on the canvas updated as well.  It should be obvious why the values in nums changed, but <u>why did the int array field in the Scores object </u><u>s also change</u>?




Ï¼ÏÏnums[0] = 9;

Ï¼ÏÏnums[1] = 8;

Ï¼ÏÏnums[2] = 7;




<strong>Part 3: Scores – toString and toStringInReverse methods </strong>

<ul>

 <li>The toString method will create a local String and then concatenate all of the values of numbers to the String.</li>

 <li>The loop above iterates as the variable i ranges from 0 through the length of numbers – 1 and then terminates (or exits) when i is no longer less than the length of the array numbers. Within the for loop above, add the number at each index to the result:</li>

 <li>Check the toString return in interactions:</li>

</ul>

Ï¼ÏÏ<strong>int</strong>[] nums = {2, 5, 8};

Ï¼ÏÏScores s = <strong>new</strong> Scores(nums);

<h1>Ï¼ÏÏs ÏÏÏÏ2  5  8  ÏÏÏ</h1>




<ul>

 <li>The toStringInReverse method will be exactly the same as toString, but will iterate from the length of numbers – 1 to 0.</li>

</ul>




Compile Scores and run the following code in the interactions pane. <strong>Do not continue until the following code runs without error in interactions. </strong>

<strong> </strong>

Ï¼ÏÏ<strong>int</strong>[] nums = {2, 5, 8};

Ï¼ÏÏScores s = <strong>new</strong> Scores(nums);

Ï¼ÏÏs.toStringInReverse()

<h1>ÏÏÏÏ8  5  2</h1>




<strong>             </strong>

<strong>Part 4: Scores – findEvens and findOdds methods </strong>

<ul>

 <li>There are two parts to the findEvens First, count the number of evens in the array:</li>

 <li>You will then need to create an array with the appropriate length to store the number of even numbers.</li>

 <li>Add the even numbers to the evens In the following loop, i represents the current index of numbers and count is the current index of evens.</li>

 <li>Compile Scores and test the return of findEvens by assigning it to an int[] evens. After the array evens has been assigned and it appears on the workbench, drag it onto your canvas window. The array does not have a toString method that includes the value at each index, so you will use a method from the util.Arrays class to display the array in interactions.</li>

</ul>

Ï¼ÏÏ<strong>import</strong> java.util.Arrays;

Ï¼ÏÏ<strong>int</strong>[] nums = {2, 5, 8, 1, 10};

Ï¼ÏÏScores s = <strong>new</strong> Scores(nums);

Ï¼ÏÏ<strong>int</strong>[] evens = s.findEvens();

Ï¼ÏÏevens <em>// toString output of an array object (will vary) </em>

ÏÏÏÏ[<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="91d5d1a4f0f3f3a6a5a7a4">[email protected]</a>

Ï¼ÏÏArrays.toString(evens)

ÏÏÏÏ[2, 8, 10]




<ul>

 <li><strong>Create </strong>the <strong>findOdds method on your own. It will perform the exact same function as </strong><strong>findEvens, but it will find all odd numbers in the array (i.e., the numbers that are not divisible by 2). </strong><em>Hint: the remainder when dividing by 2 is 1 rather than 0.</em></li>

 <li>Test findOdds in the interactions pane. After the int array odds is created, be sure to drag it from the workbench to the canvas.  <strong>Do not continue until your output is correct.</strong></li>

</ul>

Ï¼ÏÏ<strong>import</strong> java.util.Arrays;

Ï¼ÏÏ<strong>int</strong>[] nums = {1, 5, 8, 3, 10};

Ï¼ÏÏScores s = <strong>new</strong> Scores(nums);

Ï¼ÏÏ<strong>int</strong>[] odds = s.findOdds();

Arrays.toString(odds)

ÏÏÏÏ[1, 5, 3]




<strong>Part 5: Scores – </strong><strong>calculateAverage method </strong>

<ul>

 <li>First, find the sum of all values in the numbers array.</li>

</ul>

in the figure at right.

<strong>You should test all methods in the interactions pane with appropriate variables in the canvas window.  You should ensure that your methods work with a different set of values for the int array </strong><strong>nums than shown above.  </strong>




<strong>Finally, submit your Scores.java file to Web-CAT. </strong>

<strong>The canvas after dragging variables onto canvas from the Workbench and invoking the methods <em>findEvens</em>, <em>findOdds</em>, and <em>calculateAverage</em> on the Scores object <em>s.</em> </strong>