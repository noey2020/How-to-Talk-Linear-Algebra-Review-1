# How-to-Talk-Linear-Algebra-Review-1

December 24, 2020

I appreciate comments. Shoot me an email at noel_s_cruz@yahoo.com!

Hire me! 😊

- Over the past few lectures, we've been seeing vectors
and matrices more and more.
They've gradually been seeping in,
and we're not going to be able to stave them off
for very much longer.
Now I know that many of you have seen linear algebra before
at some stage, but just to be sure,
I want to do a pretty thorough review of the concepts
and skills that we're gonna be needing for this class.
Linear algebra is really the most fundamental kind
of math for machine learning,
and so it's something to understand very well.
What we'll talk about today is the basics
of representing data using vectors and matrices
and some basic notation and dot products.
So here's a dataset consisting of four points.
We can represent each of these points as vectors.
So for example this point over here is the vector (5,2),
so we can write it like this.
And this one up here is (3,5)
and the one near it is (2,4),
two along the x1 axis, four along the x2 axis,
and this one is (1,1).
We can also represent the entire dataset
in a single matrix.
So for example, we could have a matrix
in which each data point is a row.
So something like this.
[1-1, 2-4, 3-5, and 5-2].
This could be our data matrix,
and it's a matrix with four rows and two columns,
so it's a four by two matrix.
Alternatively, we could put the data points as columns.
So we could have something like [1-1, 2-4, 3-5, and 5-2].
This has two rows and four columns,
so it's a two by four matrix.
Either one is fine.
In this course, we'll mostly be adopting the convention
of doing it the first way.
So putting the data points as rows.
So let's go over some of the indexing notation.
When we have a vector is d-dimensional space,
so vector x in Rd, we'll write it as a column,
and we'll index its entries as x1 through x3.
When we have a matrix that's r by d,
that means that it's a matrix with r rows,
so r of these, and d columns, so d of these.
So it's got a total of r times d entries,
and the entry that's at row number i and column number j
will be denoted Mij.
And we'll write this as an, we'll say that its dimension
is r by d; it's an r by d matrix.
So likewise, we can describe the vector as being d by one,
d rows and one column.
Now one of the simplest things that one can do
with a vector or a matrix is simply to take the transpose,
which means to switch the rows and columns.
So for example, if we look at this vector over here,
which is a single column.
We take its transpose by just writing it as a row.
So the transpose is (1, 6, 3, 0).
So we started with something that was four by one
and we ended up with something, x transpose,
that's one by four.
Likewise, we have a matrix over here.
It has three rows and four columns,
so it's a three by four matrix.
And to take its transpose, what we can do is
we can just look at the first row of the matrix
and write it down as a column, so [1, 2, 0, 4].
And then the second row and write that down
as the second column,
and the third row and write that down as the third column.
And so it's a four by three matrix.
So formally, the transpose, A transpose,
is given by the following equation.
The ij entry of A transpose is simply the ji entry
of the original matrix.
Rows and columns are switched.
And one thing that's not hard to see
is that if you take the transpose
and then you take the transpose again,
then you end up with the original matrix.
Now how do you add or subtract vectors and matrices?
This is very simple.
You just do it element-wise.
So if you have two vectors like (1, 2, 3) and (4, 5, 6),
the way you add them is just to add them up
one element at a time.
So one plus four five.
Two plus five is seven.
Three six plus six is nine.
And it's similar with matrices.
Let's say we have two matrices, [2-1, 0-2]
and another one [1-2, 3-4].
We just add them up entry-wise.
So two plus one is three.
One plus two is three.
Zero plus three is three.
And two plus four is six.
So adding and subtracting is easy.
What's much more interesting is multiplying,
and all we'll talk about today
is the most basic kind of product,
the dot product between two vectors,
the simplest sort of product.
So let's say we have two vectors, x and y in d-dimensions,
so they each have d-coordinates.
What is the dot product between them?
Okay, so we'll denote it x dot y,
and to get the dot product,
you just multiply the corresponding entries,
so the first two numbers, x1 and y1,
the second two numbers x2 and y2, and so on,
all the way to xd times yd,
and you add all of these up.
So that's the dot product, and let's see an example.
So here we have two vectors in the two-dimensional plane.
So what are they?
x is three to the right and four up, so it's (3,4),
and y is minus four to the right and three up,
so it's (-4,3).
So this is x,
and this is y.
And what is their dot product?
So what is (3,4) dot-producted with (-4,3)?
So first we multiply the first entries,
so three times negative four,
and then we multiply the second entries, four times three.
So we get negative 12 plus 12, which is zero.
So the dot product of these two vectors is zero.
Now interestingly, looking at these two vectors,
we see that they also seem to be at right angles
to each other.
So this looks like it's 90 degrees.
Is there some relation between them being at right angles
and the dot product being zero?
Well, there definitely is.
It turns out that the dot product between two vectors
tells you the angle between them.
So here's the formula.
So take any two vectors, x and y, so we have x and y,
and the angle between them is some number theta.
It turns out that the cosine of theta is exactly
the dot product of x and y divided by the length of x
and the length of y.
So for instance, if the dot product is zero,
if we have x dot y equals zero like we had before,
that means that the cosine of theta is zero.
And what angle has a cosine of zero?
90 degrees.
We will call two vectors orthogonal
if they are at right angles to each other,
and this is gonna turn out to be a very important concept
for us.
We're gonna be using orthogonal vectors a lot.
The nice thing is that we know have a simple test
for orthogonality.
To see if two things are at right angles,
just take their dot product and check if it's equal to zero.
Another way in which we'll be using vectors
is to simply indicate directions.
So we might be interested in this direction
or that direction.
If we're merely indicating directions,
the length of the vector doesn't really matter.
So it doesn't matter if we used this direction,
or this vector, or this vector.
They all point in the same direction,
and so a common convention when one is only interested
in the direction is to normalize vectors to length one,
and that's what we call unit vectors.
So sometimes we'll be working with unit vectors,
quite often actually, and when x and y are unit vectors,
this formula for the angle becomes especially simple
because the denominator is just one.
And so we get that the cosine of the angle
is simply x dot y.
So one last thing that I want to look it
in terms of dot products and angles
is the following question.
What is x dot-producted with itself?
What is the dot product of a d-dimensional vector x
with itself?
So let's do this two different ways.
So we can do it, we can do it by just plugging it
into the formula above.
Let's try that, okay?
So x dot x is x1(x1), so x1 squared
plus x2(x2), x2 squared, all the way to xd squared.
Oh.
So this is just the length of x squared.
It's the squared Euclidean length of x.
That's x dot x.
We can also do it using the angle formula.
So what is the angle between x and itself?
It's zero, and what is the cosine of zero?
The cosine of zero is one.
So we have one equal to cosine of zero,
which is equal to x dot x over the length of x
times the length of x, and so this tells us
that x dot x is just the length of x squared,
which is the same answer we got before.
Okay, well that's it for this first portion
of our linear algebra review.
We'll be taking things slowly
because we really want to get comfortable
with this material.

I included some posts for reference.

https://github.com/noey2020/How-to-Talk-2D-Generative-Modeling

https://github.com/noey2020/How-to-Talk-Probability-Review-3

https://github.com/noey2020/How-to-Talk-Probability-Review-2

https://github.com/noey2020/How-to-Talk-Generative-Modeling-in-One-Dimension

https://github.com/noey2020/How-to-Talk-Probability-Review-1

https://github.com/noey2020/How-to-Talk-Generative-Approach-to-Classification

https://github.com/noey2020/How-to-Talk-of-Fitting-a-Distribution-to-Data-

https://github.com/noey2020/How-to-Talk-of-Host-of-Prediction-Problems

https://github.com/noey2020/How-to-Talk-of-Useful-Distance-Functions

https://github.com/noey2020/How-to-Talk-of-Improving-Nearest-Neighbor

https://github.com/noey2020/How-to-Talk-of-Prediction-Problems

https://github.com/noey2020/How-to-Talk-Matlab-Tricks-and-Tweaks

https://github.com/noey2020/How-to-Talk-Trading-and-Investing

https://github.com/noey2020/How-to-Work-in-Matlab-Development-Environment

https://github.com/noey2020/How-to-Talk-Vaccines

https://github.com/noey2020/How-to-Talk-Regression-in-Matlab

https://github.com/noey2020/How-to-Get-Started-in-Matlab

https://github.com/noey2020/How-to-Convert-Data-from-Web-Service-Using-Matlab

https://github.com/noey2020/Quote-for-the-Day

https://github.com/noey2020/How-to-Talk-Good-Investment-Strategy

https://github.com/noey2020/How-to-Talk-of-Good-Plan

https://github.com/noey2020/Thought-for-the-Day

https://github.com/noey2020/How-to-Talk-Stock-Watch-of-the-Day

https://github.com/noey2020/How-to-Talk-Data-Science

https://github.com/noey2020/How-to-Talk-Fundamental-Analysis

https://github.com/noey2020/How-to-Read-Company-Profiles

https://github.com/noey2020/How-to-Import-Data-from-Spreadsheets-and-Text-Files-Matlab-Without-Coding

https://github.com/noey2020/How-to-Talk-Model-of-Stock-Market-Prices-

https://github.com/noey2020/How-to-Talk-Digital-Wallets

https://github.com/noey2020/How-to-Talk-Investing

https://github.com/noey2020/How-to-Double-Your-Money-in-5years

https://github.com/noey2020/How-to-Talk-Matlab

I appreciate comments. Shoot me an email at noel_s_cruz@yahoo.com!
