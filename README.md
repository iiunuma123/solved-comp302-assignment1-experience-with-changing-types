Download Link: https://assignmentchef.com/product/solved-comp302-assignment1-experience-with-changing-types
<br>
Q1.  On the LearnO’Caml system we have installed <em>incorrect </em>code for the following functions:

val double : int -&gt; int = &lt;fun&gt; val fact : int -&gt; float = &lt;fun&gt;

The function “double” is supposed to take a non-negative integer <em>n </em>≥ 0 and return its value doubled. Its type is as shown above. The function “fact” is supposed to take a non-negative integer <em>n </em>≥ 0 and return <em>n</em>! as a floating-point number. We did this to give you some experience with changing types; there is no good mathematical reason for doing this<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>. The implementations we have provided may have logical, mathematical or syntactic errors. Please fix them.

Q2. ] Here is a way to compute the square root of a positive real number say <em>x</em>. We make a wild guess that the square root is some number <em>g</em>. Then we check if <em>g</em><sup>2 </sup>is close to <em>x</em>. If it is we return <em>g </em>as our answer; if not we refine our guess using the formula

<em>g</em><sup>0 </sup>= (<em>g </em>+ <em>x/g</em>)<em>/</em>2<em>.</em>0

where <em>g</em><sup>0 </sup>is the new guess. We keep repeating until we are close enough. Write an OCaml program to implement this idea. Since we are working with floating point numbers we cannot check for equality; we need to check if the numbers are close enough. I have written a function called close

1

for you as well as a function called square. In OCaml floating point operations need special symbols: you need to put a dot after the operation. Thus you need to write, for example, 2<em>.</em>0+<em>.</em>3<em>.</em>0. All the basic arithmetic operations have dotted versions: +<em>.,</em>∗<em>.,/. </em>and must be used with floating point numbers. You cannot write expressions like 2 + <em>.</em>3<em>.</em>5 or 2<em>.</em>0 + 3<em>.</em>0. We will not test your program on negative inputs so we are not requiring you to deal with the possibility that you may get a negative answer. There are of course built-in functions to compute square roots. We have written the tester program to check if you used this; <strong>you will get a zero if you use a built-in function for square roots.</strong>

Q3. This is similar to the question above except that we are computing cube roots. The formula to refine the guess is <em>g</em><sup>0 </sup>= (2<em>.</em>0 ∗ <em>g </em>+ <em>x/g</em><sup>2</sup>)<em>/</em>3<em>.</em>0

where I am using mathematical notation with arithmetic operation symbols overloaded. In your code you must use the floating-point versions of the arithmetic operations.

Q4.In lecture 1, week 2, I quickly explained the Russian peasant algorithm for fast exponentiation. In this exercise you have to implement a tail-recursive version of the algorithm. Everything is with integers in this question so please do not use floating point operations. Our tester will detect whether you used built-in functions, so please don’t try to use them.

Q5.  This question is for your spiritual growth only. Do not think it will give you extra credit or help you learn the material better. It will however stretch your brain in other directions. Do not attempt it if you have not yet finished the required homework. Do not submit a solution; please talk to me if you have solved it. Do not worry about it if you don’t understand the question.

Why do the algorithms for square root and cube root above converge? Will this kind of idea work for <em>any </em>function? What is the correct update formula for fifth roots?

<a href="#_ftnref1" name="_ftn1">[1]</a> Unless you are extending the factorial to non-integer values through the Gamma function.