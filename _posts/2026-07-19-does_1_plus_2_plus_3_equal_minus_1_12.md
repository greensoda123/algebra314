Yesterday 11:36 PM
does it have this

Then phrase it as their claim, not your own conclusion:

We can begin by assigning 
𝑆
1
S
1
	​

 the value 
1
2
2
1
	​

. In the video, Numberphile argues that because the partial sums alternate between 
1
1 and 
0
0, the sum is equal to the average of these two values, which is 
1
2
2
1
	​

.

That accurately explains what the video claims while leaving you free to criticise it in the next section. “Numberphile argues” makes it clear that you are reporting their reasoning, not agreeing with it.

could you give the new blog post with this and the zeta function well explained and stuff

Here’s a new full version. I kept the wording fairly direct, included the change about what Numberphile claims, and explained the zeta function without jumping straight into a huge formula.

Does 
1
+
2
+
3
+
4
+
⋯
1+2+3+4+⋯ really equal 
−
1
12
−
12
1
	​

?
Introduction

After reading How to Count to Infinity by Marcus du Sautoy, I became interested in infinite convergent series, such as

1
2
+
1
4
+
1
8
+
1
16
+
⋯
=
1.
2
1
	​

+
4
1
	​

+
8
1
	​

+
16
1
	​

+⋯=1.

I then widened my research by looking at divergent series, Ramanujan summation and different approaches to the expression

1
+
2
+
3
+
4
+
⋯
 
.
1+2+3+4+⋯.

A famous claim is that

1
+
2
+
3
+
4
+
⋯
=
−
1
12
.
1+2+3+4+⋯=−
12
1
	​

.

This is obviously strange because every number being added is positive. The partial sums are

1
,
 
3
,
 
6
,
 
10
,
 
15
,
 
21
,
…
1, 3, 6, 10, 15, 21,…

and they keep getting larger. Therefore, the series clearly does not converge to a negative number in the normal sense. However, 
−
1
12
−
12
1
	​

 is still connected to the series through other methods of summation.

Numberphile’s analysis

Let

𝑆
=
1
+
2
+
3
+
4
+
⋯
S=1+2+3+4+⋯

be the target series. We will also use

𝑆
1
=
1
−
1
+
1
−
1
+
1
−
1
+
⋯
S
1
	​

=1−1+1−1+1−1+⋯

and

𝑆
2
=
1
−
2
+
3
−
4
+
5
−
6
+
⋯
 
.
S
2
	​

=1−2+3−4+5−6+⋯.

The first series, 
𝑆
1
S
1
	​

, is known as Grandi’s series.

We can begin by assigning 
𝑆
1
S
1
	​

 the value 
1
2
2
1
	​

. In the video, Numberphile argues that because the partial sums alternate between 
1
1 and 
0
0, the sum is equal to the average of these two values, which is 
1
2
2
1
	​

.

Numberphile has also made [another video] showing an algebraic argument like this:

1
−
1
+
1
−
1
+
1
−
1
+
⋯
=
𝑆
1
1−1+1−1+1−1+⋯=S
1
	​

1
−
𝑆
1
=
1
−
(
1
−
1
+
1
−
1
+
1
−
1
+
⋯
 
)
1−S
1
	​

=1−(1−1+1−1+1−1+⋯)
1
−
𝑆
1
=
1
−
1
+
1
−
1
+
1
−
1
+
⋯
1−S
1
	​

=1−1+1−1+1−1+⋯
1
−
𝑆
1
=
𝑆
1
1−S
1
	​

=S
1
	​

1
=
2
𝑆
1
1=2S
1
	​

𝑆
1
=
1
2
.
S
1
	​

=
2
1
	​

.

Now that 
𝑆
1
S
1
	​

 has been assigned the value 
1
2
2
1
	​

, we can try to find 
𝑆
2
S
2
	​

 using some clever addition:

𝑆
2
	
=
1
−
2
+
3
−
4
+
5
−
6
+
⋯


𝑆
2
	
=
  
1
−
2
+
3
−
4
+
5
−
⋯
S
2
	​

S
2
	​

	​

=1−2+3−4+5−6+⋯
=1  1−2+3−4+5−⋯
	​


Adding these together gives

2
𝑆
2
=
1
−
1
+
1
−
1
+
1
−
⋯
 
.
2S
2
	​

=1−1+1−1+1−⋯.

Therefore,

2
𝑆
2
=
𝑆
1
.
2S
2
	​

=S
1
	​

.

Since 
𝑆
1
=
1
2
S
1
	​

=
2
1
	​

,

2
𝑆
2
=
1
2
2S
2
	​

=
2
1
	​


and therefore

𝑆
2
=
1
4
.
S
2
	​

=
4
1
	​

.

Finally, we can use 
𝑆
2
S
2
	​

 to find a value for the target series:

𝑆
=
1
+
2
+
3
+
4
+
5
+
6
+
⋯
S=1+2+3+4+5+6+⋯
𝑆
2
=
1
−
2
+
3
−
4
+
5
−
6
+
⋯
 
.
S
2
	​

=1−2+3−4+5−6+⋯.

Subtracting the second series from the first gives

𝑆
−
𝑆
2
=
0
+
4
+
0
+
8
+
0
+
12
+
⋯
 
.
S−S
2
	​

=0+4+0+8+0+12+⋯.

The right-hand side is four times the original series:

𝑆
−
𝑆
2
=
4
(
1
+
2
+
3
+
4
+
⋯
 
)
S−S
2
	​

=4(1+2+3+4+⋯)
𝑆
−
𝑆
2
=
4
𝑆
.
S−S
2
	​

=4S.

Using 
𝑆
2
=
1
4
S
2
	​

=
4
1
	​

,

𝑆
−
1
4
=
4
𝑆
S−
4
1
	​

=4S
−
1
4
=
3
𝑆
−
4
1
	​

=3S
𝑆
=
−
1
12
.
S=−
12
1
	​

.

Therefore, according to this argument,

1
+
2
+
3
+
4
+
⋯
=
−
1
12
.
1+2+3+4+⋯=−
12
1
	​

.
Evaluating Numberphile’s working out

The first problem is the claim that

1
−
1
+
1
−
1
+
⋯
=
1
2
.
1−1+1−1+⋯=
2
1
	​

.

Under the normal definition of an infinite sum, this is not true. The partial sums are

1
,
 
0
,
 
1
,
 
0
,
 
1
,
 
0
,
…
1, 0, 1, 0, 1, 0,…

and they never approach one particular number. Therefore, Grandi’s series is divergent.

However, the value 
1
2
2
1
	​

 is not completely made up. There are other methods that can assign values to some divergent series.

One of these is Cesàro summation. Instead of looking directly at the partial sums, it looks at their averages.

For Grandi’s series, the partial sums are

1
,
 
0
,
 
1
,
 
0
,
 
1
,
 
0
,
…
1, 0, 1, 0, 1, 0,…

and the averages of the partial sums are

1
,
 
1
2
,
 
2
3
,
 
1
2
,
 
3
5
,
 
1
2
,
…
1, 
2
1
	​

, 
3
2
	​

, 
2
1
	​

, 
5
3
	​

, 
2
1
	​

,…

These averages approach 
1
2
2
1
	​

. Therefore, Grandi’s series has a Cesàro sum of 
1
2
2
1
	​

, even though it does not have an ordinary sum.

The problem with the Numberphile argument is that this distinction is not made clear enough. Saying that the series “equals” 
1
2
2
1
	​

 makes it sound as though its partial sums converge to 
1
2
2
1
	​

, which they do not.

There are also problems with shifting, adding and subtracting the divergent series as though they were normal finite numbers. These operations are valid in many convergent series because they can be justified using limits. When the series diverge, the same rules cannot automatically be used.

The partial sums of

1
+
2
+
3
+
4
+
⋯
1+2+3+4+⋯

are given by

𝑛
(
𝑛
+
1
)
2
.
2
n(n+1)
	​

.

As 
𝑛
n becomes larger, this increases without limit. Therefore, under the ordinary definition of summation,

1
+
2
+
3
+
4
+
⋯
1+2+3+4+⋯

diverges to positive infinity. It does not converge to 
−
1
12
−
12
1
	​

.

This does not necessarily mean that the Numberphile calculation is completely useless. It produces a value that genuinely appears through other methods. However, it should not be treated as a normal proof that adding all the positive integers gives a negative answer.

Another solution for the sum of 
1
+
2
+
3
+
4
+
⋯
1+2+3+4+⋯

This comes from [blackpenredpen’s video], where he presents a student’s solution to the sum.

Start with

𝑆
=
1
+
2
+
3
+
4
+
5
+
6
+
7
+
8
+
9
+
10
+
11
+
12
+
13
+
14
+
15
+
16
+
⋯
 
.
S=1+2+3+4+5+6+7+8+9+10+11+12+13+14+15+16+⋯.

The terms are grouped like this:

𝑆
=
1
+
(
2
+
3
+
4
)
+
(
5
+
6
+
7
)
+
(
8
+
9
+
10
)
+
(
11
+
12
+
13
)
+
(
14
+
15
+
16
)
+
⋯
 
.
S=1+(2+3+4)+(5+6+7)+(8+9+10)+(11+12+13)+(14+15+16)+⋯.

The groups have the values

2
+
3
+
4
=
9
,
2+3+4=9,
5
+
6
+
7
=
18
,
5+6+7=18,
8
+
9
+
10
=
27
,
8+9+10=27,
11
+
12
+
13
=
36.
11+12+13=36.

Therefore,

𝑆
=
1
+
9
+
18
+
27
+
36
+
⋯
S=1+9+18+27+36+⋯
𝑆
=
1
+
9
(
1
+
2
+
3
+
4
+
⋯
 
)
S=1+9(1+2+3+4+⋯)
𝑆
=
1
+
9
𝑆
S=1+9S
−
8
𝑆
=
1
−8S=1
𝑆
=
−
1
8
.
S=−
8
1
	​

.

The video then shows another grouping:

𝑆
=
1
+
2
+
3
+
4
+
5
+
6
+
7
+
8
+
9
+
10
+
11
+
12
+
13
+
14
+
15
+
16
+
17
+
⋯
S=1+2+3+4+5+6+7+8+9+10+11+12+13+14+15+16+17+⋯
𝑆
=
(
1
+
2
)
+
(
3
+
4
+
5
+
6
+
7
)
+
(
8
+
9
+
10
+
11
+
12
)
+
(
13
+
14
+
15
+
16
+
17
)
+
⋯
 
.
S=(1+2)+(3+4+5+6+7)+(8+9+10+11+12)+(13+14+15+16+17)+⋯.

The sums of the groups are

3
,
 
25
,
 
50
,
 
75
,
…
3, 25, 50, 75,…

so

𝑆
=
3
+
25
+
50
+
75
+
⋯
S=3+25+50+75+⋯
𝑆
=
3
+
25
(
1
+
2
+
3
+
4
+
⋯
 
)
S=3+25(1+2+3+4+⋯)
𝑆
=
3
+
25
𝑆
S=3+25S
−
24
𝑆
=
3
−24S=3
𝑆
=
−
3
24
S=−
24
3
	​

𝑆
=
−
1
8
.
S=−
8
1
	​

.

The problem with this solution is that 
𝑆
S is being treated as if it were an ordinary finite number.

For example, the equation

𝑆
=
1
+
9
𝑆
S=1+9S

can only be rearranged to give 
𝑆
=
−
1
8
S=−
8
1
	​

 if 
𝑆
S is an actual finite value. However, the original series does not have a finite ordinary sum.

Grouping the terms does not fix this. The new series

1
+
9
+
18
+
27
+
36
+
⋯
1+9+18+27+36+⋯

still increases without limit. The same is true for

3
+
25
+
50
+
75
+
⋯
 
.
3+25+50+75+⋯.

This method gives

𝑆
=
−
1
8
,
S=−
8
1
	​

,

while the Numberphile method gives

𝑆
=
−
1
12
.
S=−
12
1
	​

.

The same series cannot have two different ordinary sums. This shows that normal algebraic rules cannot be freely used on divergent series.

The fact that the working looks reasonable does not mean it is valid. Once a divergent infinite series is treated as though it were a normal number, it becomes possible to produce contradictory answers.

The Riemann zeta function

The value 
−
1
12
−
12
1
	​

 can be connected to the series more properly using the Riemann zeta function.

The zeta function is first defined by

𝜁
(
𝑠
)
=
1
1
𝑠
+
1
2
𝑠
+
1
3
𝑠
+
1
4
𝑠
+
⋯
 
.
ζ(s)=
1
s
1
	​

+
2
s
1
	​

+
3
s
1
	​

+
4
s
1
	​

+⋯.

This can also be written as

𝜁
(
𝑠
)
=
∑
𝑛
=
1
∞
1
𝑛
𝑠
.
ζ(s)=
n=1
∑
∞
	​

n
s
1
	​

.

For example, when 
𝑠
=
2
s=2,

𝜁
(
2
)
=
1
+
1
4
+
1
9
+
1
16
+
⋯
 
.
ζ(2)=1+
4
1
	​

+
9
1
	​

+
16
1
	​

+⋯.

This series converges, and its value is

𝜁
(
2
)
=
𝜋
2
6
.
ζ(2)=
6
π
2
	​

.

However, the infinite-series definition of the zeta function only converges when the real part of 
𝑠
s is greater than 
1
1.

If we directly substitute 
𝑠
=
−
1
s=−1, we get

𝜁
(
−
1
)
=
1
1
−
1
+
1
2
−
1
+
1
3
−
1
+
⋯
ζ(−1)=
1
−1
1
	​

+
2
−1
1
	​

+
3
−1
1
	​

+⋯

which becomes

𝜁
(
−
1
)
=
1
+
2
+
3
+
4
+
⋯
 
.
ζ(−1)=1+2+3+4+⋯.

But this substitution is not valid using the original series definition because the series diverges at 
𝑠
=
−
1
s=−1.

To find a value for 
𝜁
(
−
1
)
ζ(−1), the zeta function must first be extended using something called analytic continuation.

What is analytic continuation?

A simpler example can be seen using the geometric series

1
+
𝑥
+
𝑥
2
+
𝑥
3
+
⋯
 
.
1+x+x
2
+x
3
+⋯.

When 
∣
𝑥
∣
<
1
∣x∣<1, this converges to

1
1
−
𝑥
.
1−x
1
	​

.

For example, if 
𝑥
=
1
2
x=
2
1
	​

,

1
+
1
2
+
1
4
+
1
8
+
⋯
=
2
1+
2
1
	​

+
4
1
	​

+
8
1
	​

+⋯=2

and

1
1
−
1
2
=
2.
1−
2
1
	​

1
	​

=2.

The series and the formula give the same result.

However, the expression

1
1
−
𝑥
1−x
1
	​


also has values outside the range 
∣
𝑥
∣
<
1
∣x∣<1. For example, when 
𝑥
=
2
x=2,

1
1
−
2
=
−
1.
1−2
1
	​

=−1.

This does not mean that

1
+
2
+
4
+
8
+
⋯
=
−
1.
1+2+4+8+⋯=−1.

The series on the left still diverges. It only means that the function represented by the series inside its region of convergence can be extended beyond that region.

The same general idea is used with the zeta function. Its original infinite series only works when the real part of 
𝑠
s is greater than 
1
1, but analytic continuation extends the function to almost every other complex number.

The extended function agrees with the original zeta function wherever the original series converges. It also gives values at places where the original series does not converge.

The main exception is 
𝑠
=
1
s=1, where the zeta function has a singularity.

Using analytic continuation,

𝜁
(
−
1
)
=
−
1
12
.
ζ(−1)=−
12
1
	​

.

This does not mean that the partial sums of 
1
+
2
+
3
+
4
+
⋯
1+2+3+4+⋯ approach 
−
1
12
−
12
1
	​

. It means that the analytically continued zeta function has the value 
−
1
12
−
12
1
	​

 at 
𝑠
=
−
1
s=−1.

How can 
𝜁
(
−
1
)
ζ(−1) be found?

One way to make the connection clearer is to use the Dirichlet eta function.

The eta function is defined by the alternating series

𝜂
(
𝑠
)
=
1
−
1
2
𝑠
+
1
3
𝑠
−
1
4
𝑠
+
⋯
 
.
η(s)=1−
2
s
1
	​

+
3
s
1
	​

−
4
s
1
	​

+⋯.

It is connected to the zeta function by

𝜂
(
𝑠
)
=
(
1
−
2
1
−
𝑠
)
𝜁
(
𝑠
)
.
η(s)=(1−2
1−s
)ζ(s).

The alternating expression

1
−
2
+
3
−
4
+
5
−
6
+
⋯
1−2+3−4+5−6+⋯

can be assigned the value 
1
4
4
1
	​

 using Abel summation.

To see where this comes from, begin with the geometric series

1
−
𝑥
+
𝑥
2
−
𝑥
3
+
𝑥
4
−
⋯
=
1
1
+
𝑥
,
1−x+x
2
−x
3
+x
4
−⋯=
1+x
1
	​

,

which is valid for 
∣
𝑥
∣
<
1
∣x∣<1.

Differentiating both sides gives

−
1
+
2
𝑥
−
3
𝑥
2
+
4
𝑥
3
−
⋯
=
−
1
(
1
+
𝑥
)
2
.
−1+2x−3x
2
+4x
3
−⋯=−
(1+x)
2
1
	​

.

Multiplying both sides by 
−
1
−1 gives

1
−
2
𝑥
+
3
𝑥
2
−
4
𝑥
3
+
⋯
=
1
(
1
+
𝑥
)
2
.
1−2x+3x
2
−4x
3
+⋯=
(1+x)
2
1
	​

.

As 
𝑥
x approaches 
1
1 from below, the right-hand side approaches

1
(
1
+
1
)
2
=
1
4
.
(1+1)
2
1
	​

=
4
1
	​

.

Therefore, in the Abel-summed sense,

1
−
2
+
3
−
4
+
5
−
⋯
=
1
4
.
1−2+3−4+5−⋯=
4
1
	​

.

Now use

𝜂
(
𝑠
)
=
(
1
−
2
1
−
𝑠
)
𝜁
(
𝑠
)
.
η(s)=(1−2
1−s
)ζ(s).

At 
𝑠
=
−
1
s=−1,

𝜂
(
−
1
)
=
(
1
−
2
1
−
(
−
1
)
)
𝜁
(
−
1
)
.
η(−1)=(1−2
1−(−1)
)ζ(−1).

Therefore,

𝜂
(
−
1
)
=
(
1
−
2
2
)
𝜁
(
−
1
)
η(−1)=(1−2
2
)ζ(−1)
𝜂
(
−
1
)
=
−
3
𝜁
(
−
1
)
.
η(−1)=−3ζ(−1).

Using the regularised value

𝜂
(
−
1
)
=
1
4
,
η(−1)=
4
1
	​

,

we get

1
4
=
−
3
𝜁
(
−
1
)
4
1
	​

=−3ζ(−1)

and therefore

𝜁
(
−
1
)
=
−
1
12
.
ζ(−1)=−
12
1
	​

.

This is much closer to a proper explanation of why 
−
1
12
−
12
1
	​

 appears. It still uses an extended form of summation and analytic continuation, but the rules being used are defined rather than just treating divergent series like normal numbers.

Ramanujan summation

Ramanujan summation gives another way of associating a finite value with a divergent series.

It does not say that the ordinary partial sums converge. Instead, it attempts to separate the main divergent part of the sum and leave behind a finite remainder.

One version of the formula used in [blackpenredpen’s video] is

𝑓
(
0
)
2
+
∑
𝑛
=
1
∞
𝑓
(
𝑛
)
=
𝑅
𝑖
∫
0
∞
𝑓
(
𝑖
𝑡
)
−
𝑓
(
−
𝑖
𝑡
)
𝑒
2
𝜋
𝑡
−
1
 
𝑑
𝑡
.
2
f(0)
	​

+
n=1
∑
∞
	​

f(n)
=
R
i∫
0
∞
	​

e
2πt
−1
f(it)−f(−it)
	​

dt.

The 
𝑅
R above the equals sign is important. It shows that this is a Ramanujan-summed value, not an ordinary sum.

For

1
+
2
+
3
+
4
+
⋯
 
,
1+2+3+4+⋯,

we let

𝑓
(
𝑥
)
=
𝑥
.
f(x)=x.

Since 
𝑓
(
0
)
=
0
f(0)=0,

1
+
2
+
3
+
4
+
⋯
=
𝑅
𝑖
∫
0
∞
𝑖
𝑡
−
(
−
𝑖
𝑡
)
𝑒
2
𝜋
𝑡
−
1
 
𝑑
𝑡
.
1+2+3+4+⋯
=
R
i∫
0
∞
	​

e
2πt
−1
it−(−it)
	​

dt.

Since

𝑖
𝑡
−
(
−
𝑖
𝑡
)
=
2
𝑖
𝑡
,
it−(−it)=2it,

we get

1
+
2
+
3
+
4
+
⋯
=
𝑅
−
2
∫
0
∞
𝑡
𝑒
2
𝜋
𝑡
−
1
 
𝑑
𝑡
.
1+2+3+4+⋯
=
R
−2∫
0
∞
	​

e
2πt
−1
t
	​

dt.

Using the substitution

𝑢
=
2
𝜋
𝑡
,
u=2πt,

we have

𝑡
=
𝑢
2
𝜋
t=
2π
u
	​


and

𝑑
𝑡
=
𝑑
𝑢
2
𝜋
.
dt=
2π
du
	​

.

Therefore,

−
2
∫
0
∞
𝑡
𝑒
2
𝜋
𝑡
−
1
 
𝑑
𝑡
=
−
1
2
𝜋
2
∫
0
∞
𝑢
𝑒
𝑢
−
1
 
𝑑
𝑢
.
−2∫
0
∞
	​

e
2πt
−1
t
	​

dt=−
2π
2
1
	​

∫
0
∞
	​

e
u
−1
u
	​

du.

There is a known result

∫
0
∞
𝑢
𝑒
𝑢
−
1
 
𝑑
𝑢
=
Γ
(
2
)
𝜁
(
2
)
.
∫
0
∞
	​

e
u
−1
u
	​

du=Γ(2)ζ(2).

We know that

Γ
(
2
)
=
1
Γ(2)=1

and

𝜁
(
2
)
=
𝜋
2
6
.
ζ(2)=
6
π
2
	​

.

Therefore,

∫
0
∞
𝑢
𝑒
𝑢
−
1
 
𝑑
𝑢
=
𝜋
2
6
.
∫
0
∞
	​

e
u
−1
u
	​

du=
6
π
2
	​

.

Substituting this into the earlier result gives

1
+
2
+
3
+
4
+
⋯
=
𝑅
−
1
2
𝜋
2
×
𝜋
2
6
1+2+3+4+⋯
=
R
−
2π
2
1
	​

×
6
π
2
	​

1
+
2
+
3
+
4
+
⋯
=
𝑅
−
1
12
.
1+2+3+4+⋯
=
R
−
12
1
	​

.

Again, this does not mean that the ordinary series converges to 
−
1
12
−
12
1
	​

. The 
𝑅
R above the equals sign shows that this is the Ramanujan-summed value.

Conclusion

Under the normal definition of an infinite sum,

1
+
2
+
3
+
4
+
⋯
1+2+3+4+⋯

does not equal 
−
1
12
−
12
1
	​

. Its partial sums increase without limit, so the series diverges to positive infinity.

The popular Numberphile argument produces 
−
1
12
−
12
1
	​

, but it uses algebraic operations on divergent series without properly explaining which type of summation is being used. The alternative 
−
1
8
−
8
1
	​

 argument shows why this is dangerous, because different groupings can produce different answers.

However, 
−
1
12
−
12
1
	​

 is not a random number. It appears when the Riemann zeta function is analytically continued to 
𝑠
=
−
1
s=−1, and it is also produced by Ramanujan summation.

Therefore, writing

1
+
2
+
3
+
4
+
⋯
=
−
1
12
1+2+3+4+⋯=−
12
1
	​


without any explanation is misleading.

A more accurate statement would be

𝜁
(
−
1
)
=
−
1
12
,
ζ(−1)=−
12
1
	​

,

or

1
+
2
+
3
+
4
+
⋯
=
𝑅
−
1
12
.
1+2+3+4+⋯
=
R
−
12
1
	​

.

The series does not converge normally, but 
−
1
12
−
12
1
	​

 is a regularised value that can still be useful in mathematics and physics.

Today 11:49 AM
blackpenredpen's ramanujan sum video https://www.youtube.com/watch?v=U_g_OZLt4OU
numberphiles astounding 1+2+3+... = -1/12: https://www.youtube.com/watch?v=w-I6XTVZXww
bprp's -1/8 video https://youtu.be/6FTwMUL69u0?si=_qTgn-2UoyCUVIPc
numberphiles other video: https://www.youtube.com/watch?v=PCu_BNNI5x4

previous blog md file so you understand the latex:
---
layout: post
title: "Why Does the Double Domino Effect Require Precise Spacing?"
date: 2026-04-16
---

## Introduction

While watching one of [Zack D. Films’ videos on the double domino effect](https://www.youtube.com/watch?v=TXOZWq5hGJg), I became curious about how far apart dominoes could be placed while still allowing the chain to continue.

After experimenting with this in Algodoo, I noticed something surprising.

A spacing of 14.5 cm was too small for the double domino effect to occur, yet increasing it slightly to 15.0 cm allowed the entire sequence to continue.

At first glance, this seems counterintuitive. Since both values are below the maximum possible spacing, the domino effect occurs in each case. Why, then, does such a small change determine whether the double domino effect takes place?

This led me to investigate the mathematics behind the domino effect.

## The problem

Consider a row of identical rectangular bricks, each of height $h$ and width $w$, standing upright and equally spaced.

If one brick is pushed, it falls and hits the next, creating a domino effect.

But this raises the question:

**how far apart can the bricks be while still allowing the chain to continue, and under what conditions does the double domino effect occur?**

---

## The Geometry of a Falling Brick

Focus on a single brick rotating about its bottom corner.

As it falls through an angle $\theta$ from the vertical, the top corner moves both downward and horizontally.

The horizontal position of the top corner relative to the pivot is

$x = h \sin\theta + w \cos\theta$

The next brick begins at a horizontal distance of $w + d$, where $d$ is the gap between bricks.

For the falling brick to just touch the next one, these must be equal:

$h \sin\theta + w \cos\theta = w + d$

Rearranging gives

$d = h \sin\theta + w(\cos\theta - 1)$

This equation describes how the gap $d$ depends on the angle $\theta$ at which contact occurs.

---

## The Maximum Possible Gap

To find the largest possible spacing, we maximise

$d(\theta) = h \sin\theta + w(\cos\theta - 1)$

Differentiating:

$\frac{dd}{d\theta} = h \cos\theta - w \sin\theta$

Setting this equal to zero:

$h \cos\theta = w \sin\theta$

so

$\tan\theta = \frac{h}{w}$

Substituting this back into the expression for $d$ leads to

$d_{\max} = \sqrt{h^2 + w^2} - w$

This is the **maximum spacing** for which the falling brick can still reach the next one.

---

## A Numerical Example

In the UK, the standard dimensions for a brick are height $h = 21.5$  cm and width $w = 6.5$  cm:

$d_{\max} = \sqrt{21.5^2 + 6.5^2} - 6.5$

$= \sqrt{504.5} - 6.5$

$\approx 22.46 - 6.5 = 15.96 \text{  cm}$

So the bricks cannot be spaced more than approximately $15.96$  cm apart.

---

## Online simulation

To test this, I simulated the system in Algodoo.

At a spacing of $15.0$  cm, the chain successfully continues:

![Domino effect](/assets/domino_150.gif)

What I find interesting is that the distances between the bricks had to be very precise for the double domino effect to take place. For example, 15.0 cm distance works pretty well, but 14.7 cm was too small for there to be enough space for the bricks to fall cleanly.

Even though the simulation looks rather simple, the precision required for success took a while to fully accomplish. If you are interested in this Algodoo scene I used for this simulation, feel free to email me (more information on the [About page](https://www.algebra314.com/about/)).

---

## Conclusion

The domino effect is not just a visual curiosity, but a combination of geometry and mechanics.

The maximum spacing

$d_{\max} = \sqrt{h^2 + w^2} - w$

comes from considering how far a rotating brick can reach.

However, the success of the chain depends not only on whether the bricks touch, but on how much energy is transferred during the collision.

This explains why the “best” spacing is often close to, but not exactly equal to, the theoretical maximum.

make an md version of this blog then i can adjust it to my liking

Worked for 3m 30s

Done. It uses the same YAML front matter and LaTeX style as your previous blog, with all four video links included.

does_1_plus_2_plus_3_equal_minus_1_12.md 

Library
/
does_1_plus_2_plus_3_equal_minus_1_12.md
---
layout: post
title: "Does 1 + 2 + 3 + ... Really Equal -1/12?"
date: 2026-07-19
---

## Introduction

After reading *How to Count to Infinity* by Marcus du Sautoy, I became interested in infinite convergent series, such as

$\frac12+\frac14+\frac18+\frac1{16}+\cdots=1$

I then widened my research by looking at divergent series, Ramanujan summation and different approaches to the expression

$1+2+3+4+\cdots$

A famous claim is that

$1+2+3+4+\cdots=-\frac1{12}$

This is clearly strange because every number being added is positive. The partial sums are

$1,\ 3,\ 6,\ 10,\ 15,\ 21,\ldots$

and they keep getting larger. Therefore, the series does not converge to a negative number in the normal sense.

So why is $-\frac1{12}$ connected to it at all?

---

## Numberphile's analysis

One of the most well-known explanations comes from [Numberphile's video](https://www.youtube.com/watch?v=w-I6XTVZXww).

Let

$S=1+2+3+4+\cdots$

be the target series. We will also use the two series

$S_1=1-1+1-1+1-1+\cdots$

and

$S_2=1-2+3-4+5-6+\cdots$

The first series, $S_1$, is known as **Grandi's series**.

We can begin by assigning $S_1$ the value $\frac12$. In the video, Numberphile argues that because the partial sums alternate between 1 and 0, the sum is equal to the average of these two values, which is $\frac12$.

Numberphile has also made [another video](https://www.youtube.com/watch?v=PCu_BNNI5x4) showing an algebraic argument like this:

$1-1+1-1+1-1+\cdots=S_1$

$1-S_1=1-(1-1+1-1+1-1+\cdots)$

$1-S_1=1-1+1-1+1-1+\cdots$

$1-S_1=S_1$

$1=2S_1$

$S_1=\frac12$

Now that $S_1$ has been assigned the value $\frac12$, we can try to find $S_2$ using some clever addition. We write a second copy of $S_2$ shifted one place to the right:

$$
\begin{array}{rcrrrrrrr}
S_2&=&1&-2&+3&-4&+5&-\cdots\\
S_2&=&&1&-2&+3&-4&+\cdots\\
\hline
2S_2&=&1&-1&+1&-1&+1&-\cdots
\end{array}
$$

Therefore,

$2S_2=S_1$

Since $S_1=\frac12$,

$2S_2=\frac12$

$S_2=\frac14$

Finally, we can use $S_2$ to find a value for the target series:

$$
\begin{array}{rcrrrrrrr}
S&=&1&+2&+3&+4&+5&+6+\cdots\\
S_2&=&1&-2&+3&-4&+5&-6+\cdots\\
\hline
S-S_2&=&0&+4&+0&+8&+0&+12+\cdots
\end{array}
$$

The right-hand side is four times the original series:

$S-S_2=4(1+2+3+4+\cdots)$

$S-S_2=4S$

Using $S_2=\frac14$ gives

$S-\frac14=4S$

$-\frac14=3S$

$S=-\frac1{12}$

Therefore, according to this argument,

$1+2+3+4+\cdots=-\frac1{12}$

---

## Evaluating Numberphile's working out

At the start, we assigned $S_1$ the value $\frac12$. However, under the normal definition of convergence, this is not the sum of the series.

The partial sums of Grandi's series are

$1,\ 0,\ 1,\ 0,\ 1,\ 0,\ldots$

They repeatedly alternate between 1 and 0 and never approach one particular value. Therefore, the series diverges.

However, the value $\frac12$ is not completely made up. There are methods that assign values to certain divergent series, and one of these is **Cesàro summation**.

Instead of only looking at the partial sums, Cesàro summation looks at their averages. The running averages of

$1,\ 0,\ 1,\ 0,\ 1,\ 0,\ldots$

are

$1,\ \frac12,\ \frac23,\ \frac12,\ \frac35,\ \frac12,\ldots$

These averages approach $\frac12$. This means that Grandi's series has a **Cesàro sum** of $\frac12$, even though it does not have an ordinary sum.

The distinction matters. Saying

$1-1+1-1+\cdots=\frac12$

without explanation makes it look as though the partial sums converge to $\frac12$, which they do not.

There is also a problem with shifting, adding and subtracting divergent series as though they are ordinary finite numbers. These operations can be justified for convergent series using limits, but the same rules cannot automatically be used when a series diverges.

The partial sums of the target series are

$1,\ 3,\ 6,\ 10,\ 15,\ldots$

The sum of the first $n$ positive integers is

$S_n=\frac{n(n+1)}2$

As $n$ becomes larger, this increases without limit. Therefore,

$1+2+3+4+\cdots$

diverges to positive infinity under ordinary summation. It does not normally converge to $-\frac1{12}$.

The Numberphile calculation still produces a value that genuinely appears through other methods, but it should not be treated as a normal proof that adding every positive integer gives a negative answer.

---

## Another solution for the sum of $1+2+3+4+\cdots$

Another strange solution comes from [blackpenredpen's video](https://youtu.be/6FTwMUL69u0?si=_qTgn-2UoyCUVIPc), where he presents a student's solution to the sum.

Start with

$S=1+2+3+4+5+6+7+8+9+10+11+12+13+14+15+16+\cdots$

The terms are grouped like this:

$S=1+(2+3+4)+(5+6+7)+(8+9+10)+(11+12+13)+(14+15+16)+\cdots$

The groups have the values

$2+3+4=9$

$5+6+7=18$

$8+9+10=27$

$11+12+13=36$

Therefore,

$S=1+9+18+27+36+\cdots$

$S=1+9(1+2+3+4+\cdots)$

$S=1+9S$

$-8S=1$

$S=-\frac18$

The video then gives another grouping:

$S=1+2+3+4+5+6+7+8+9+10+11+12+13+14+15+16+17+\cdots$

$S=(1+2)+(3+4+5+6+7)+(8+9+10+11+12)+(13+14+15+16+17)+\cdots$

The sums of these groups are

$3,\ 25,\ 50,\ 75,\ldots$

so

$S=3+25+50+75+\cdots$

$S=3+25(1+2+3+4+\cdots)$

$S=3+25S$

$-24S=3$

$S=-\frac3{24}$

$S=-\frac18$

The problem with this solution is that $S$ is being treated as though it is an ordinary finite number.

For example, the equation

$S=1+9S$

can only be rearranged to give $S=-\frac18$ if $S$ is a finite value that behaves normally under algebra. However, the original series has no finite ordinary sum.

Grouping the terms does not stop the series from diverging. The new series

$1+9+18+27+36+\cdots$

still increases without limit. The same is true for

$3+25+50+75+\cdots$

This method gives

$S=-\frac18$

while the Numberphile method gives

$S=-\frac1{12}$

The same series cannot have two different ordinary sums. The contradiction shows why divergent series cannot be freely rearranged and then treated like normal numbers.

The algebra looks familiar, but the assumptions behind it are not valid here.

---

## So where does $-\frac1{12}$ actually come from?

The value $-\frac1{12}$ can be connected to the series more properly using the **Riemann zeta function**.

The zeta function is first defined by

$\zeta(s)=\frac1{1^s}+\frac1{2^s}+\frac1{3^s}+\frac1{4^s}+\cdots$

or, more compactly,

$\zeta(s)=\sum_{n=1}^{\infty}\frac1{n^s}$

For example, when $s=2$,

$\zeta(2)=1+\frac14+\frac19+\frac1{16}+\cdots$

This series converges, and its value is

$\zeta(2)=\frac{\pi^2}{6}$

However, the infinite-series definition of the zeta function only converges when the real part of $s$ is greater than 1.

If we try to substitute $s=-1$, we get

$\zeta(-1)=\frac1{1^{-1}}+\frac1{2^{-1}}+\frac1{3^{-1}}+\cdots$

which becomes

$\zeta(-1)=1+2+3+4+\cdots$

The problem is that the series definition is not valid at $s=-1$, because the series diverges there.

To find a value for $\zeta(-1)$, the zeta function has to be extended using **analytic continuation**. The original series defines the function in the region where it converges, and analytic continuation extends that same function to other values of $s$. The extended zeta function agrees with the original wherever the original series works, but it is also defined at almost every other complex number. Its main exception is $s=1$.

A more detailed definition can be found in the [NIST Digital Library of Mathematical Functions](https://dlmf.nist.gov/25.2).

---

## A simpler example of analytic continuation

A simpler version of this idea can be seen using the geometric series

$1+x+x^2+x^3+\cdots=\frac1{1-x}$

This series only converges when $|x|<1$.

For example, when $x=\frac12$,

$1+\frac12+\frac14+\frac18+\cdots=2$

and

$\frac1{1-\frac12}=2$

The series and the formula agree.

However, the expression

$\frac1{1-x}$

also has values outside the range $|x|<1$. If $x=2$, then

$\frac1{1-2}=-1$

This does **not** mean that

$1+2+4+8+\cdots=-1$

The series still diverges. It only means that the function represented by the geometric series inside its region of convergence continues to exist outside that region.

The same basic distinction applies to the zeta function. The series

$\sum_{n=1}^{\infty}\frac1{n^s}$

does not converge at $s=-1$, but the function that it defines for $\operatorname{Re}(s)>1$ can be analytically continued to $s=-1$.

For the continued zeta function,

$\zeta(-1)=-\frac1{12}$

This does not mean that the partial sums $1,3,6,10,\ldots$ approach $-\frac1{12}$. It means that the analytically continued zeta function has that value at $s=-1$.

---

## Finding $\zeta(-1)$ using an alternating series

One way of seeing where the value comes from is to use the **Dirichlet eta function**:

$\eta(s)=1-\frac1{2^s}+\frac1{3^s}-\frac1{4^s}+\cdots$

The eta and zeta functions are connected by

$\eta(s)=(1-2^{1-s})\zeta(s)$

The alternating series that appears when $s=-1$ is

$1-2+3-4+5-6+\cdots$

This also diverges normally, but it can be assigned the value $\frac14$ using **Abel summation**.

Begin with the geometric series

$1-x+x^2-x^3+x^4-\cdots=\frac1{1+x}$

which converges when $|x|<1$.

Differentiate both sides:

$-1+2x-3x^2+4x^3-\cdots=-\frac1{(1+x)^2}$

Multiplying by $-1$ gives

$1-2x+3x^2-4x^3+\cdots=\frac1{(1+x)^2}$

Now let $x$ approach 1 from below. The series is still being approached through values where it converges, while the right-hand side approaches

$\frac1{(1+1)^2}=\frac14$

Therefore, in the Abel-summed sense,

$1-2+3-4+5-\cdots=\frac14$

Now use

$\eta(s)=(1-2^{1-s})\zeta(s)$

At $s=-1$,

$\eta(-1)=(1-2^{1-(-1)})\zeta(-1)$

$\eta(-1)=(1-2^2)\zeta(-1)$

$\eta(-1)=-3\zeta(-1)$

Using the regularised value $\eta(-1)=\frac14$,

$\frac14=-3\zeta(-1)$

and therefore

$\zeta(-1)=-\frac1{12}$

This is much closer to a proper explanation of why $-\frac1{12}$ appears. We are still not claiming that the original series converges. Instead, the value comes from extending the zeta function and using a defined method of summation.

---

## Ramanujan summation

Ramanujan summation gives another way of associating a finite value with a divergent series.

It does not claim that the normal partial sums approach a finite number. Instead, it removes the main divergent part and keeps a finite remainder.

In [blackpenredpen's Ramanujan summation video](https://www.youtube.com/watch?v=U_g_OZLt4OU), the regularised sum is found using a formula closely connected to the [Abel--Plana formula](https://dlmf.nist.gov/2.10):

$$
\frac{f(0)}2+\sum_{n=1}^{\infty}f(n)
\overset{R}{=}
i\int_0^\infty
\frac{f(it)-f(-it)}{e^{2\pi t}-1}\,dt
$$

The $R$ above the equals sign is important. It shows that this is a Ramanujan-regularised value rather than an ordinary sum.

For

$1+2+3+4+\cdots$

we let

$f(x)=x$

Since $f(0)=0$,

$$
1+2+3+4+\cdots
\overset{R}{=}
i\int_0^\infty
\frac{it-(-it)}{e^{2\pi t}-1}\,dt
$$

As

$it-(-it)=2it$

and

$i(2it)=-2t$

we get

$$
1+2+3+4+\cdots
\overset{R}{=}
-2\int_0^\infty
\frac{t}{e^{2\pi t}-1}\,dt
$$

Now use the substitution

$u=2\pi t$

This gives

$t=\frac{u}{2\pi}$

and

$dt=\frac{du}{2\pi}$

Therefore,

$$
-2\int_0^\infty
\frac{t}{e^{2\pi t}-1}\,dt
=
-\frac1{2\pi^2}
\int_0^\infty
\frac{u}{e^u-1}\,du
$$

There is a standard connection between this integral, the gamma function and the zeta function:

$$
\int_0^\infty\frac{u^{s-1}}{e^u-1}\,du
=
\Gamma(s)\zeta(s)
$$

For $s=2$,

$$
\int_0^\infty\frac{u}{e^u-1}\,du
=
\Gamma(2)\zeta(2)
$$

The gamma function extends the factorial, with

$\Gamma(n)=(n-1)!$

so

$\Gamma(2)=1$

We also know that

$\zeta(2)=\frac{\pi^2}{6}$

Therefore,

$$
\int_0^\infty\frac{u}{e^u-1}\,du
=
\frac{\pi^2}{6}
$$

Substituting this into the earlier result gives

$$
1+2+3+4+\cdots
\overset{R}{=}
-\frac1{2\pi^2}\times\frac{\pi^2}{6}
$$

and therefore

$$
1+2+3+4+\cdots
\overset{R}{=}
-\frac1{12}
$$

Again, this does not mean that the ordinary series converges to $-\frac1{12}$. The symbol above the equals sign shows that a different method of summation is being used.

The zeta-regularised value and the Ramanujan-regularised value agree for this series, although they are not exactly the same method in general.

---

## Conclusion

Under the normal definition of an infinite sum,

$1+2+3+4+\cdots$

does not equal $-\frac1{12}$. Its partial sums increase without limit, so the series diverges to positive infinity.

The popular Numberphile argument reaches $-\frac1{12}$, but it manipulates divergent series in a way that is not valid under ordinary summation. The alternative $-\frac18$ solution shows the problem clearly, because another apparently reasonable grouping gives a completely different answer.

However, $-\frac1{12}$ is not a random value. It appears when the Riemann zeta function is analytically continued to $s=-1$, and it also appears through Ramanujan summation.

Therefore, writing

$1+2+3+4+\cdots=-\frac1{12}$

without any explanation is misleading.

More accurate statements would be

$\zeta(-1)=-\frac1{12}$

or

$$
1+2+3+4+\cdots
\overset{R}{=}
-\frac1{12}
$$

The ordinary series diverges, but $-\frac1{12}$ is a regularised value that can still be associated with it.

Library
/
does_1_plus_2_plus_3_equal_minus_1_12.md
---
layout: post
title: "Does 1 + 2 + 3 + ... Really Equal -1/12?"
date: 2026-07-19
---

## Introduction

After reading *How to Count to Infinity* by Marcus du Sautoy, I became interested in infinite convergent series, such as

$\frac12+\frac14+\frac18+\frac1{16}+\cdots=1$

I then widened my research by looking at divergent series, Ramanujan summation and different approaches to the expression

$1+2+3+4+\cdots$

A famous claim is that

$1+2+3+4+\cdots=-\frac1{12}$

This is clearly strange because every number being added is positive. The partial sums are

$1,\ 3,\ 6,\ 10,\ 15,\ 21,\ldots$

and they keep getting larger. Therefore, the series does not converge to a negative number in the normal sense.

So why is $-\frac1{12}$ connected to it at all?

---

## Numberphile's analysis

One of the most well-known explanations comes from [Numberphile's video](https://www.youtube.com/watch?v=w-I6XTVZXww).

Let

$S=1+2+3+4+\cdots$

be the target series. We will also use the two series

$S_1=1-1+1-1+1-1+\cdots$

and

$S_2=1-2+3-4+5-6+\cdots$

The first series, $S_1$, is known as **Grandi's series**.

We can begin by assigning $S_1$ the value $\frac12$. In the video, Numberphile argues that because the partial sums alternate between 1 and 0, the sum is equal to the average of these two values, which is $\frac12$.

Numberphile has also made [another video](https://www.youtube.com/watch?v=PCu_BNNI5x4) showing an algebraic argument like this:

$1-1+1-1+1-1+\cdots=S_1$

$1-S_1=1-(1-1+1-1+1-1+\cdots)$

$1-S_1=1-1+1-1+1-1+\cdots$

$1-S_1=S_1$

$1=2S_1$

$S_1=\frac12$

Now that $S_1$ has been assigned the value $\frac12$, we can try to find $S_2$ using some clever addition. We write a second copy of $S_2$ shifted one place to the right:

$$
\begin{array}{rcrrrrrrr}
S_2&=&1&-2&+3&-4&+5&-\cdots\\
S_2&=&&1&-2&+3&-4&+\cdots\\
\hline
2S_2&=&1&-1&+1&-1&+1&-\cdots
\end{array}
$$

Therefore,

$2S_2=S_1$

Since $S_1=\frac12$,

$2S_2=\frac12$

$S_2=\frac14$

Finally, we can use $S_2$ to find a value for the target series:

$$
\begin{array}{rcrrrrrrr}
S&=&1&+2&+3&+4&+5&+6+\cdots\\
S_2&=&1&-2&+3&-4&+5&-6+\cdots\\
\hline
S-S_2&=&0&+4&+0&+8&+0&+12+\cdots
\end{array}
$$

The right-hand side is four times the original series:

$S-S_2=4(1+2+3+4+\cdots)$

$S-S_2=4S$

Using $S_2=\frac14$ gives

$S-\frac14=4S$

$-\frac14=3S$

$S=-\frac1{12}$

Therefore, according to this argument,

$1+2+3+4+\cdots=-\frac1{12}$

---

## Evaluating Numberphile's working out

At the start, we assigned $S_1$ the value $\frac12$. However, under the normal definition of convergence, this is not the sum of the series.

The partial sums of Grandi's series are

$1,\ 0,\ 1,\ 0,\ 1,\ 0,\ldots$

They repeatedly alternate between 1 and 0 and never approach one particular value. Therefore, the series diverges.

However, the value $\frac12$ is not completely made up. There are methods that assign values to certain divergent series, and one of these is **Cesàro summation**.

Instead of only looking at the partial sums, Cesàro summation looks at their averages. The running averages of

$1,\ 0,\ 1,\ 0,\ 1,\ 0,\ldots$

are

$1,\ \frac12,\ \frac23,\ \frac12,\ \frac35,\ \frac12,\ldots$

These averages approach $\frac12$. This means that Grandi's series has a **Cesàro sum** of $\frac12$, even though it does not have an ordinary sum.

The distinction matters. Saying

$1-1+1-1+\cdots=\frac12$

without explanation makes it look as though the partial sums converge to $\frac12$, which they do not.

There is also a problem with shifting, adding and subtracting divergent series as though they are ordinary finite numbers. These operations can be justified for convergent series using limits, but the same rules cannot automatically be used when a series diverges.

The partial sums of the target series are

$1,\ 3,\ 6,\ 10,\ 15,\ldots$

The sum of the first $n$ positive integers is

$S_n=\frac{n(n+1)}2$

As $n$ becomes larger, this increases without limit. Therefore,

$1+2+3+4+\cdots$

diverges to positive infinity under ordinary summation. It does not normally converge to $-\frac1{12}$.

The Numberphile calculation still produces a value that genuinely appears through other methods, but it should not be treated as a normal proof that adding every positive integer gives a negative answer.

---

## Another solution for the sum of $1+2+3+4+\cdots$

Another strange solution comes from [blackpenredpen's video](https://youtu.be/6FTwMUL69u0?si=_qTgn-2UoyCUVIPc), where he presents a student's solution to the sum.

Start with

$S=1+2+3+4+5+6+7+8+9+10+11+12+13+14+15+16+\cdots$

The terms are grouped like this:

$S=1+(2+3+4)+(5+6+7)+(8+9+10)+(11+12+13)+(14+15+16)+\cdots$

The groups have the values

$2+3+4=9$

$5+6+7=18$

$8+9+10=27$

$11+12+13=36$

Therefore,

$S=1+9+18+27+36+\cdots$

$S=1+9(1+2+3+4+\cdots)$

$S=1+9S$

$-8S=1$

$S=-\frac18$

The video then gives another grouping:

$S=1+2+3+4+5+6+7+8+9+10+11+12+13+14+15+16+17+\cdots$

$S=(1+2)+(3+4+5+6+7)+(8+9+10+11+12)+(13+14+15+16+17)+\cdots$

The sums of these groups are

$3,\ 25,\ 50,\ 75,\ldots$

so

$S=3+25+50+75+\cdots$

$S=3+25(1+2+3+4+\cdots)$

$S=3+25S$

$-24S=3$

$S=-\frac3{24}$

$S=-\frac18$

The problem with this solution is that $S$ is being treated as though it is an ordinary finite number.

For example, the equation

$S=1+9S$

can only be rearranged to give $S=-\frac18$ if $S$ is a finite value that behaves normally under algebra. However, the original series has no finite ordinary sum.

Grouping the terms does not stop the series from diverging. The new series

$1+9+18+27+36+\cdots$

still increases without limit. The same is true for

$3+25+50+75+\cdots$

This method gives

$S=-\frac18$

while the Numberphile method gives

$S=-\frac1{12}$

The same series cannot have two different ordinary sums. The contradiction shows why divergent series cannot be freely rearranged and then treated like normal numbers.

The algebra looks familiar, but the assumptions behind it are not valid here.

---

## So where does $-\frac1{12}$ actually come from?

The value $-\frac1{12}$ can be connected to the series more properly using the **Riemann zeta function**.

The zeta function is first defined by

$\zeta(s)=\frac1{1^s}+\frac1{2^s}+\frac1{3^s}+\frac1{4^s}+\cdots$

or, more compactly,

$\zeta(s)=\sum_{n=1}^{\infty}\frac1{n^s}$

For example, when $s=2$,

$\zeta(2)=1+\frac14+\frac19+\frac1{16}+\cdots$

This series converges, and its value is

$\zeta(2)=\frac{\pi^2}{6}$

However, the infinite-series definition of the zeta function only converges when the real part of $s$ is greater than 1.

If we try to substitute $s=-1$, we get

$\zeta(-1)=\frac1{1^{-1}}+\frac1{2^{-1}}+\frac1{3^{-1}}+\cdots$

which becomes

$\zeta(-1)=1+2+3+4+\cdots$

The problem is that the series definition is not valid at $s=-1$, because the series diverges there.

To find a value for $\zeta(-1)$, the zeta function has to be extended using **analytic continuation**. The original series defines the function in the region where it converges, and analytic continuation extends that same function to other values of $s$. The extended zeta function agrees with the original wherever the original series works, but it is also defined at almost every other complex number. Its main exception is $s=1$.

A more detailed definition can be found in the [NIST Digital Library of Mathematical Functions](https://dlmf.nist.gov/25.2).

---

## A simpler example of analytic continuation

A simpler version of this idea can be seen using the geometric series

$1+x+x^2+x^3+\cdots=\frac1{1-x}$

This series only converges when $|x|<1$.

For example, when $x=\frac12$,

$1+\frac12+\frac14+\frac18+\cdots=2$

and

$\frac1{1-\frac12}=2$

The series and the formula agree.

However, the expression

$\frac1{1-x}$

also has values outside the range $|x|<1$. If $x=2$, then

$\frac1{1-2}=-1$

This does **not** mean that

$1+2+4+8+\cdots=-1$

The series still diverges. It only means that the function represented by the geometric series inside its region of convergence continues to exist outside that region.

The same basic distinction applies to the zeta function. The series

$\sum_{n=1}^{\infty}\frac1{n^s}$

does not converge at $s=-1$, but the function that it defines for $\operatorname{Re}(s)>1$ can be analytically continued to $s=-1$.

For the continued zeta function,

$\zeta(-1)=-\frac1{12}$

This does not mean that the partial sums $1,3,6,10,\ldots$ approach $-\frac1{12}$. It means that the analytically continued zeta function has that value at $s=-1$.

---

## Finding $\zeta(-1)$ using an alternating series

One way of seeing where the value comes from is to use the **Dirichlet eta function**:

$\eta(s)=1-\frac1{2^s}+\frac1{3^s}-\frac1{4^s}+\cdots$

The eta and zeta functions are connected by

$\eta(s)=(1-2^{1-s})\zeta(s)$

The alternating series that appears when $s=-1$ is

$1-2+3-4+5-6+\cdots$

This also diverges normally, but it can be assigned the value $\frac14$ using **Abel summation**.

Begin with the geometric series

$1-x+x^2-x^3+x^4-\cdots=\frac1{1+x}$

which converges when $|x|<1$.

Differentiate both sides:

$-1+2x-3x^2+4x^3-\cdots=-\frac1{(1+x)^2}$

Multiplying by $-1$ gives

$1-2x+3x^2-4x^3+\cdots=\frac1{(1+x)^2}$

Now let $x$ approach 1 from below. The series is still being approached through values where it converges, while the right-hand side approaches

$\frac1{(1+1)^2}=\frac14$

Therefore, in the Abel-summed sense,

$1-2+3-4+5-\cdots=\frac14$

Now use

$\eta(s)=(1-2^{1-s})\zeta(s)$

At $s=-1$,

$\eta(-1)=(1-2^{1-(-1)})\zeta(-1)$

$\eta(-1)=(1-2^2)\zeta(-1)$

$\eta(-1)=-3\zeta(-1)$

Using the regularised value $\eta(-1)=\frac14$,

$\frac14=-3\zeta(-1)$

and therefore

$\zeta(-1)=-\frac1{12}$

This is much closer to a proper explanation of why $-\frac1{12}$ appears. We are still not claiming that the original series converges. Instead, the value comes from extending the zeta function and using a defined method of summation.

---

## Ramanujan summation

Ramanujan summation gives another way of associating a finite value with a divergent series.

It does not claim that the normal partial sums approach a finite number. Instead, it removes the main divergent part and keeps a finite remainder.

In [blackpenredpen's Ramanujan summation video](https://www.youtube.com/watch?v=U_g_OZLt4OU), the regularised sum is found using a formula closely connected to the [Abel--Plana formula](https://dlmf.nist.gov/2.10):

$$
\frac{f(0)}2+\sum_{n=1}^{\infty}f(n)
\overset{R}{=}
i\int_0^\infty
\frac{f(it)-f(-it)}{e^{2\pi t}-1}\,dt
$$

The $R$ above the equals sign is important. It shows that this is a Ramanujan-regularised value rather than an ordinary sum.

For

$1+2+3+4+\cdots$

we let

$f(x)=x$

Since $f(0)=0$,

$$
1+2+3+4+\cdots
\overset{R}{=}
i\int_0^\infty
\frac{it-(-it)}{e^{2\pi t}-1}\,dt
$$

As

$it-(-it)=2it$

and

$i(2it)=-2t$

we get

$$
1+2+3+4+\cdots
\overset{R}{=}
-2\int_0^\infty
\frac{t}{e^{2\pi t}-1}\,dt
$$

Now use the substitution

$u=2\pi t$

This gives

$t=\frac{u}{2\pi}$

and

$dt=\frac{du}{2\pi}$

Therefore,

$$
-2\int_0^\infty
\frac{t}{e^{2\pi t}-1}\,dt
=
-\frac1{2\pi^2}
\int_0^\infty
\frac{u}{e^u-1}\,du
$$

There is a standard connection between this integral, the gamma function and the zeta function:

$$
\int_0^\infty\frac{u^{s-1}}{e^u-1}\,du
=
\Gamma(s)\zeta(s)
$$

For $s=2$,

$$
\int_0^\infty\frac{u}{e^u-1}\,du
=
\Gamma(2)\zeta(2)
$$

The gamma function extends the factorial, with

$\Gamma(n)=(n-1)!$

so

$\Gamma(2)=1$

We also know that

$\zeta(2)=\frac{\pi^2}{6}$

Therefore,

$$
\int_0^\infty\frac{u}{e^u-1}\,du
=
\frac{\pi^2}{6}
$$

Substituting this into the earlier result gives

$$
1+2+3+4+\cdots
\overset{R}{=}
-\frac1{2\pi^2}\times\frac{\pi^2}{6}
$$

and therefore

$$
1+2+3+4+\cdots
\overset{R}{=}
-\frac1{12}
$$

Again, this does not mean that the ordinary series converges to $-\frac1{12}$. The symbol above the equals sign shows that a different method of summation is being used.

The zeta-regularised value and the Ramanujan-regularised value agree for this series, although they are not exactly the same method in general.

---

## Conclusion

Under the normal definition of an infinite sum,

$1+2+3+4+\cdots$

does not equal $-\frac1{12}$. Its partial sums increase without limit, so the series diverges to positive infinity.

The popular Numberphile argument reaches $-\frac1{12}$, but it manipulates divergent series in a way that is not valid under ordinary summation. The alternative $-\frac18$ solution shows the problem clearly, because another apparently reasonable grouping gives a completely different answer.

However, $-\frac1{12}$ is not a random value. It appears when the Riemann zeta function is analytically continued to $s=-1$, and it also appears through Ramanujan summation.

Therefore, writing

$1+2+3+4+\cdots=-\frac1{12}$

without any explanation is misleading.

More accurate statements would be

$\zeta(-1)=-\frac1{12}$

or

$$
1+2+3+4+\cdots
\overset{R}{=}
-\frac1{12}
$$

The ordinary series diverges, but $-\frac1{12}$ is a regularised value that can still be associated with it.
