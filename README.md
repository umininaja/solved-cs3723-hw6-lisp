Download Link: https://assignmentchef.com/product/solved-cs3723-hw6-lisp
<br>



Code the functions listed below and use the specified test cases.  If you cheat on this assignment, you will most likely do poorly with the LISP coding on the final exam.

Notes:

<ul>

 <li>Look at the set up information for more information on executing LISP files.</li>

 <li>The <strong>only</strong> functions you can use are either those we discussed in the LISP notes (including ones we developed as exercises) or you can reuse any of the functions developed below in subsequent functions.</li>

 <li>Place your code in hw6Lisp.txt.</li>

 <li>Load your code using (load “hw6Lisp.txt” :echo T :print T).</li>

 <li>To execute the test cases using the file I provided:(load “hw6LispRun.txt” :echo T :print T)</li>

 <li>Your functions must be executed on a <strong>fox</strong> server using the specified test cases.</li>

 <li>Turn in a zip file named LastNameFirstName.zip (no spaces) containing:

  <ul>

   <li>Your source LISP code (hw6Lisp.txt)</li>

   <li>Your log of the session. Select all the text in the terminal window and paste it into a file named hw6Out.txt</li>

   <li>Do not have any directories within your zip file.</li>

  </ul></li>

 <li>In Blackboard, include a note that specifies whether you did the extra credit.</li>

</ul>




<ol>

 <li>Code the function, removeNILTop, which is passed a list and removes NIL at the top level.</li>

</ol>

Examples:

&gt; (removeNILTop ‘(NIL X NIL NIL Y NIL Z))

(X Y Z)

&gt; (removeNILTop ‘(X NIL Y NIL Z NIL))

(X Y Z)

&gt; (removeNILTop ‘(NIL (X NIL Y) (NIL NIL)))

((X NIL Y) (NIL NIL))




<ol start="2">

 <li>Code the function, removeNILMost, which is passed a list and removes NIL at any level. Note: if the result of removing NIL gives a NIL, it is unnecessary to remove that resulting NIL. (See the extra credit.)</li>

</ol>

Examples:

&gt; (removeNILMost ‘(NIL X NIL NIL Y NIL Z))

(X Y Z)

&gt; (removeNILMost ‘(X NIL (Y NIL Z) NIL))

(X (Y Z))

&gt; (removeNILMost ‘(NIL (NIL) (X NIL Y) (NIL NIL) Z))

(NIL (X Y) NIL Z)

&gt; (removeNILMost ‘(NIL ((((((NIL) NIL)))))))

((((((NIL))))))




<ol start="3">

 <li>Code the function, reverseTop, which is passed a list and returns a reversed list of the high-level entries. Do not use the built-in REVERSE function.</li>

</ol>

Hint:  APPEND could be useful.

Examples:

&gt; (reverseTop ‘(X Y Z))

(Z Y X)

&gt; (reverseTop ‘(X (Y Z (A)) (W)))

((W) (Y Z (A)) X)




<ol start="4">

 <li>Code the function, reverseAll, which is passed a list and returns a reversed list at all levels.</li>

</ol>

Examples:

&gt; (reverseAll ‘(X Y Z))

(Z Y X)

&gt; (reverseAll ‘(X (Y Z (A)) (W)))

((W) ((A) Z Y) X)




<ol start="5">

 <li>Code the function, palindrome, which is passed a list and returns T if the list is a palindrome; otherwise, it returns NIL. It only needs to be a palindrome at the top-level.</li>

</ol>

Examples:

&gt; (palindrome ‘(R A C E C A R))

T

&gt; (palindrome ‘(W A S I T A C A R O R A C A T I S A W))

T

&gt; (palindrome ‘(N I X O N))

NIL

<strong> </strong>

<strong>Extra credit:</strong> (5 pts)

Code the function removeNILAll which also removes any resulting NIL (except the single outermost)

&gt; (removeNILAll ‘(NIL (NIL) (X NIL Y) (NIL NIL) Z))

((X Y) Z)

&gt; (removeNILAll ‘(NIL ((((((NIL) NIL)))))))

NIL




To receive extra credit:

<ul>

 <li>removeNILAll must work for all possible cases.</li>

 <li>The other functions must work for all possible cases.</li>

 <li>All your functions must be properly documented.</li>

 <li>Your submission MUST NOT be late.</li>

 <li>There is an extra file to run your code that includes extra credit cases named “hw6LispExtraRun.txt”</li>

</ul>