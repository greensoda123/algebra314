---
layout: post
title: "The Congruent Number Problem: From Right-Angled Triangles to Elliptic Curves"
date: 2026-06-23
---

This post is about the **congruent number problem**, which is a millennium-old mathematical question that asks which positive integers can be expressed as the area of a right-angled triangle where all the side lengths are rational, meaning they can be expressed as fractions.

The problem may initially appear simple, but it has never been completely solved after more than a thousand years of study. The aim of this post is to explore why this simple-looking problem is difficult, starting with rational Pythagorean triples and examples of congruent numbers, before moving on to algorithms, elliptic curves, the modern progress on the problem, and why mathematicians still have not been able to fully solve the problem.

Overall, this post will show how a question about triangle areas can lead to deeper areas of mathematics.

## What is a congruent number?

For a right-angled triangle, let the side lengths be $a$, $b$, and $c$, where $c$ is the hypotenuse. Then:

$a^2+b^2=c^2$

and the area is:

$\frac{1}{2}ab=n$

![A general right-angled triangle with side lengths a, b, c and area n](/assets/general-triangle.png)

Where $a$ and $b$ are the adjacent/opposite side lengths, $c$ is the hypotenuse, and $n$ is the area.

The congruent number problem asks us what are the values of $n$ where:

$n \in \mathbb{Z}^+$

and:

$a,b,c \in \mathbb{Q}^+$

In other words, we want to know which positive integers can be the area of a right-angled triangle whose side lengths are positive rational numbers.

For our first example, take a right-angled triangle where the opposite, adjacent, and hypotenuse lengths are $(3,4,5)$, which are all rational, positive integers. The area of this triangle is:

$\frac{1}{2}(3)(4)=6$

showing that $6$ is congruent and therefore $n=6$ is a solution.

![A 3, 4, 5 triangle with area 6](/assets/345-triangle.png)

$(3,4,5)$ is an example of a **Pythagorean triple**, which is defined as a set of 3 positive integers that can be used as the side lengths of a right-angled triangle.

In other words, a Pythagorean triple is any set of values $(a,b,c)$ where:

$a^2+b^2=c^2$

and:

$a,b,c \in \mathbb{Z}^+$

We can use Pythagorean triples to find rational Pythagorean triangles, giving us solutions for congruent numbers. For example:

- $(5,12,13)$ is a Pythagorean triple since:

$5^2+12^2=13^2$

and $5,12,13 \in \mathbb{Z}^+$.

This gives us a triangle with area:

$\frac{1}{2}(5)(12)=30$

therefore $30$ is a congruent number.

![A 5, 12, 13 triangle with area 30](/assets/51213-triangle.png)

Another example is $(40,9,41)$, which is a Pythagorean triple because:

$40^2+9^2=41^2$

This gives us a triangle with area:

$\frac{1}{2}(40)(9)=180$

therefore $180$ is a congruent number.

![A 40, 9, 41 triangle with area 180](/assets/40941-triangle.png)

However, to find congruent numbers using this method, it is better if we do not limit ourselves to the side lengths being integers. Instead, we should use any positive rational number for the side lengths, so that we can find more congruent numbers.

This means that we can use sets such as:

$\left(\frac{20}{3},\frac{3}{2},\frac{41}{6}\right)$

which will give us a triangle with area:

$\frac{1}{2}\left(\frac{20}{3}\right)\left(\frac{3}{2}\right)=5$

meaning $5$ is a congruent number, which we are now able to prove.

If we take a closer look, multiplying all the lengths in our:

$\left(\frac{20}{3},\frac{3}{2},\frac{41}{6}\right)$

triangle by $6$ gets us $(40,9,41)$, which is a Pythagorean triple we defined earlier.

The area of the:

$\left(\frac{20}{3},\frac{3}{2},\frac{41}{6}\right)$

triangle is $5$, and the area of the $(40,9,41)$ triangle is $180$.

![A rational triangle with area 5 scaled by 6 into the 40, 9, 41 triangle with area 180](/assets/scaling-triangles.png)

Do you notice any pattern? When we multiplied the lengths by $6$, we multiplied the area by $6^2$. This means that scaling the sides of a triangle by a factor scales the area of the triangle by the square of that factor.

We can use this observation to create a statement:

> $N$ is congruent if and only if $M=d^2N$ is also congruent, where $M$ is the larger scaled area, $N$ is the smaller area, $d$ is the length scale factor, and $d^2$ is the area scale factor.

We can use this to construct an algorithm to find congruent numbers. First, find a Pythagorean triple, then calculate its area. If the area contains a square factor, the triangle can be scaled down to remove this square factor, producing a rational right-angled triangle with a smaller area. This smaller area is then a congruent number.

We can use this on our $(40,9,41)$ triangle. For example:

$n=\frac{1}{2}(40)(9)=180$

Now find the square factors of $180$:

$180=2^2\times 3^2\times 5$

$180=(2\times 3)^2\times 5$

$180=6^2\times 5$

Hence the square factors of $180$ are $2^2$, $3^2$, and $6^2$. $1$ is also a square factor, but it does not help us with finding new congruent numbers since any number divided by 1 is itself, so we ignore it.

We can use this to find congruent numbers by dividing $180$ by each square factor.

Scaling the area down by $2^2$:

$(2^2\times 3^2\times 5)\div 2^2=3^2\times 5=45$

Hence we have found a congruent number $45$.

Doing the same with $3^2$:

$(2^2\times 3^2\times 5)\div 3^2=2^2\times 5=20$

Hence $20$ is congruent.

Finally, doing the same with $6^2$:

$(6^2\times 5)\div 6^2=5$

Hence we have now found the congruent numbers $5$, $20$, $45$, and $180$ by using this algorithm on $180$.

Repeat this with another appropriate triple to find all the possible congruent numbers you can derive from its area.

## Generating Pythagorean triples

The algorithm works, but we need a large amount of Pythagorean triples in order to use it, so we now need to derive an algorithm that produces Pythagorean triples.

We want integer side lengths $a,b,c$ satisfying:

$a^2+b^2=c^2$

Rearrange:

$c^2-a^2=b^2$

Factorise:

$(c-a)(c+a)=b^2$

We need two factors whose product is a square. To do this, write:

$c-a=2l^2$

and:

$c+a=2k^2$

We use $2l^2$ and $2k^2$ because for a primitive Pythagorean triple, $c$ must be odd and exactly one of $a$ or $b$ must be even. Taking $a$ to be the odd shorter side, both $c-a$ and $c+a$ are even, meaning that $c-a$ and $c+a$ are multiples of $2$. Since:

$(c-a)(c+a)=b^2$

we need their product to be a square, so we choose to write them as $2l^2$ and $2k^2$.

We can use this to find $a$, $b$, and $c$ for our algorithm.

Finding $b$:

$b^2=(c-a)(c+a)$

$b^2=(2l^2)(2k^2)$

$b^2=4k^2l^2$

$b=2kl$

Finding $c$:

$(c-a)+(c+a)=2l^2+2k^2$

$2c=2l^2+2k^2$

$c=k^2+l^2$

Finding $a$:

$(c+a)-(c-a)=2k^2-2l^2$

$2a=2k^2-2l^2$

$a=k^2-l^2$

Therefore, Pythagorean triples can be parametrised by:

$(k^2-l^2,2kl,k^2+l^2)$

where:

$k,l>0, \quad k>l, \quad \gcd(k,l)=1$

and $k$ and $l$ have different parity.

This ensures that the algorithm produces primitive Pythagorean triples.

The first condition, $k,l>0$, ensures that the side lengths are positive, as in a triangle, you cannot have a side length that is negative or $0$.

The second condition, $k>l$, is needed because $k^2-l^2$ is one of the side lengths, and this side length would not be positive if $k\leq l$ when $k,l>0$.

The third condition, $\gcd(k,l)=1$, means that the greatest common factor between the sides is $1$. This is crucial as it prevents the triple from being a scaled-up version of a smaller triple.

The fourth condition, that $k$ and $l$ have different parity, means that one is even and the other is odd. This is needed because it prevents the side lengths from sharing a common factor. For example:

- Let $k=5$ and $l=3$
- Both are odd, so they do not have a different parity
- $k^2-l^2=25-9=16$
- $2kl=2(5)(3)=30$
- $k^2+l^2=25+9=34$
- This gives us a triple $(16,30,34)$
- However, they all share a common factor of $2$, since $(16,30,34)$ is equal to $2(8,15,17)$
- Because they share a common factor of $2$, they are not primitive
- This means that without this condition, we will get scaled-up versions of Pythagorean triples rather than primitive ones, which is why this condition is needed

By using different values of $k$ and $l$ that satisfy the conditions, we can find primitive Pythagorean triples.

Now we can complete the full congruent number algorithm, as we have found an algorithm to find all congruent numbers that can be derived from a given Pythagorean triple, and an algorithm that produces primitive Pythagorean triples.

Using the completed algorithm, we can create a table:

| $k$ | $l$ | Triple $(a,b,c)$ | Area $\frac{1}{2}ab$ | Congruent number(s) |
|---:|---:|---:|---:|---:|
| 2 | 1 | $(3,4,5)$ | 6 | 6 |
| 4 | 1 | $(15,8,17)$ | 60 | 60, 15 |
| 3 | 2 | $(5,12,13)$ | 30 | 30 |
| 6 | 1 | $(35,12,37)$ | 210 | 210 |
| 5 | 2 | $(21,20,29)$ | 210 | 210 |
| 4 | 3 | $(7,24,25)$ | 84 | 84, 21 |
| 8 | 1 | $(63,16,65)$ | 504 | 504, 126, 56, 14 |
| 7 | 2 | $(45,28,53)$ | 630 | 630, 70 |
| 5 | 4 | $(9,40,41)$ | 180 | 180, 45, 20, 5 |

Showing all the calculations for this algorithm in the main post would take up too much space, so I will do 2 examples to show the process.

### Example with k = 4 and l = 3

Take:

$k=4, \quad l=3$

These satisfy the 4 conditions for $k$ and $l$, where:

$k,l>0, \quad k>l, \quad \gcd(k,l)=1$

and $k$ and $l$ have different parity, so we can continue.

Using:

$(k^2-l^2,2kl,k^2+l^2)$

we get:

$k^2-l^2=16-9=7$

$2kl=2(4)(3)=24$

$k^2+l^2=16+9=25$

Hence we have a primitive Pythagorean triple $(7,24,25)$.

Using the area formula:

$\frac{1}{2}ab$

we get:

$\frac{1}{2}(7)(24)=84$

This means that $84$ is a congruent number.

Using our first statement, $N$ is congruent if and only if $M=d^2N$, we can see if there are any other congruent numbers we can derive from $84$:

$84=2^2\times 3\times 7$

$84$ has a square factor of $2^2$, so we can scale the area down by $2^2$ to find a new congruent number:

$84\div 2^2=84\div 4=21$

So with $k=4$ and $l=3$, we have found the congruent numbers $84$ and $21$.

### Example with k = 3 and l = 2

Take:

$k=3, \quad l=2$

These satisfy the 4 conditions for $k$ and $l$ we defined earlier, so we can continue.

Using:

$(k^2-l^2,2kl,k^2+l^2)$

we get:

$k^2-l^2=9-4=5$

$2kl=2(3)(2)=12$

$k^2+l^2=9+4=13$

Hence we have a primitive Pythagorean triple $(5,12,13)$.

Using the area formula:

$\frac{1}{2}ab$

we get:

$\frac{1}{2}(5)(12)=30$

This means that $30$ is a congruent number.

Using our first statement, $N$ is congruent if and only if $M=d^2N$, we can see if there are any other congruent numbers we can derive from $30$:

$30=2\times 3\times 5$

There are no square factors, so $30$ is the only congruent number we can get from this triple.

## Why the algorithm is limited

This algorithm initially seems pretty nice, but it does have issues that become very obvious the more you use it, and this is why many mathematicians say that this is a “bad” algorithm.

Such issues include:

- The algorithm only produces examples of congruent numbers rather than giving us a systematic order of congruent numbers. This means that it is difficult to tell whether a certain number is congruent, as it may take a very long time to find it using the algorithm, or it may never appear.
- Repetition of congruent integers. For example, $210$ appears twice in the table, and this will continue to happen if you use the algorithm.
- $53$ is congruent, but it only appears for the first time when $k=1873180325$ and $l=1158313156$.

Before we continue, it is important to disclose that not all numbers are congruent. So far, the algorithm has only helped find examples of congruent numbers. However, the congruent number problem is not just about finding examples, it is also about proving when a number is not congruent. This is much harder, because finding one rational triangle proves that a number is congruent, but proving that no rational triangle exists requires ruling out every possible rational triangle.

For example, here are the congruent numbers up to $30$:

$5,6,7,13,14,15,20,21,22,23,24,26,28,30$

A pattern is that there are no square numbers. Fermat used infinite descent to prove that no square numbers are congruent.

Instead of the algorithm, let’s try another approach.

## Turning the problem into an elliptic curve

We want rational numbers $a,b,c$ where:

$a^2+b^2=c^2$

and:

$\frac{1}{2}ab=n$

Rearrange Pythagoras:

$b^2=c^2-a^2$

Factorise:

$b^2=(c-a)(c+a)$

Now rewrite $c+a$ as:

$c+a=(c-a)+2a$

This gives:

$b^2=(c-a)((c-a)+2a)$

Therefore:

$b^2=(c-a)^2+2a(c-a)$

From the area formula:

$\frac{1}{2}ab=n$

we get:

$a=\frac{2n}{b}$

Substitute this into the equation:

$b^2=(c-a)^2+2a(c-a)$

This gives:

$b^2=(c-a)^2+2\left(\frac{2n}{b}\right)(c-a)$

So:

$b^2=(c-a)^2+\frac{4n}{b}(c-a)$

Multiply both sides by $b$:

$b^3=b(c-a)^2+4n(c-a)$

Now this is the part where it is easy to skip too quickly. We want to turn this into the elliptic curve:

$y^2=x^3-n^2x$

To do this, multiply both sides by:

$\frac{n^3}{(c-a)^3}$

So:

$\frac{n^3b^3}{(c-a)^3} = \frac{n^3b(c-a)^2}{(c-a)^3} + \frac{4n^4(c-a)}{(c-a)^3}$

Now simplify each part.

The left-hand side becomes:

$\frac{n^3b^3}{(c-a)^3} = \left(\frac{nb}{c-a}\right)^3$

The first term on the right-hand side becomes:

$\frac{n^3b(c-a)^2}{(c-a)^3} = \frac{n^3b}{c-a} = n^2\left(\frac{nb}{c-a}\right)$

The second term on the right-hand side becomes:

$\frac{4n^4(c-a)}{(c-a)^3} = \frac{4n^4}{(c-a)^2} = \left(\frac{2n^2}{c-a}\right)^2$

So the equation becomes:

$\left(\frac{nb}{c-a}\right)^3 = n^2\left(\frac{nb}{c-a}\right) + \left(\frac{2n^2}{c-a}\right)^2$

Rearrange this to put the squared term on the left:

$\left(\frac{2n^2}{c-a}\right)^2 = \left(\frac{nb}{c-a}\right)^3 - n^2\left(\frac{nb}{c-a}\right)$

Now let:

$x=\frac{nb}{c-a}$

and:

$y=\frac{2n^2}{c-a}$

Then:

$y^2=x^3-n^2x$

The equation:

$y^2=x^3-n^2x$

defines an **elliptic curve**. This equation is important because it changes the congruent number problem from a problem about finding rational side lengths of triangles into a problem about finding rational points on this curve.

Instead of searching directly for $a$, $b$, and $c$, we can now search for rational values of $x$ and $y$ satisfying:

$y^2=x^3-n^2x$

where $y\neq 0$.

## Going back from the curve to the triangle

Finding $a,b,c$ in terms of $x,y,n$:

First, find $b$. We have:

$y=\frac{2n^2}{c-a}$

so:

$c-a=\frac{2n^2}{y}$

Also:

$x=\frac{nb}{c-a}$

Substitute $c-a=\frac{2n^2}{y}$:

$x=\frac{nb}{\frac{2n^2}{y}}$

$x=nb\cdot \frac{y}{2n^2}$

$x=\frac{by}{2n}$

Therefore:

$b=\frac{2nx}{y}$

Now find $a$. Since:

$\frac{1}{2}ab=n$

we have:

$ab=2n$

Substitute:

$b=\frac{2nx}{y}$

so:

$a\left(\frac{2nx}{y}\right)=2n$

$\frac{ax}{y}=1$

Therefore:

$a=\frac{y}{x}$

But since:

$y^2=x^3-n^2x$

we can write:

$y^2=x(x^2-n^2)$

Divide by $x$:

$\frac{y^2}{x}=x^2-n^2$

Then divide by $y$:

$\frac{y}{x}=\frac{x^2-n^2}{y}$

so:

$a=\frac{x^2-n^2}{y}$

Now find $c$. We already have:

$c-a=\frac{2n^2}{y}$

so:

$c=a+\frac{2n^2}{y}$

Substitute:

$a=\frac{x^2-n^2}{y}$

This gives:

$c=\frac{x^2-n^2}{y}+\frac{2n^2}{y}$

$c=\frac{x^2+n^2}{y}$

Therefore:

$(a,b,c)=\left(\frac{x^2-n^2}{y},\frac{2nx}{y},\frac{x^2+n^2}{y}\right)$

There is a correspondence between rational right-angled triangles with area $n$ and rational points on the curve:

$y^2=x^3-n^2x$

where $y\neq 0$. This means that every rational triangle with area $n$ gives a rational point on the curve, and every rational point on the curve with $y\neq 0$ gives a rational triangle with area $n$, as long as we take the corresponding positive side lengths.

We use the condition $y\neq 0$ because points with $y=0$ do not produce valid triangles. From the formula:

$(a,b,c)=\left(\frac{x^2-n^2}{y},\frac{2nx}{y},\frac{x^2+n^2}{y}\right)$

$y$ is the denominator, and we cannot have a length where the denominator is $0$.

## Example with n = 6

A right-angled triangle with lengths $(3,4,5)$ gives us area:

$\frac{1}{2}(3)(4)=6$

So:

$a=3, \quad b=4, \quad c=5, \quad n=6$

Using:

$x=\frac{nb}{c-a}$

we get:

$x=\frac{6\cdot4}{5-3}=12$

Using:

$y=\frac{2n^2}{c-a}$

we get:

$y=\frac{2\cdot6^2}{5-3}=36$

So:

$(3,4,5)\rightarrow(12,36)$

Now check that $(12,36)$ lies on the curve:

$y^2=x^3-36x$

Substitute $x=12$ and $y=36$:

$36^2=12^3-36(12)$

$1296=1728-432=1296$

So $(12,36)$ is a rational point on:

$y^2=x^3-36x$

Now reverse the process:

$a=\frac{x^2-n^2}{y}$

$a=\frac{12^2-6^2}{36}=3$

$b=\frac{2nx}{y}$

$b=\frac{2(6)(12)}{36}=4$

$c=\frac{x^2+n^2}{y}$

$c=\frac{12^2+6^2}{36}=5$

So:

$(12,36)\rightarrow(3,4,5)$

This shows the correspondence in practice: the triangle and the point contain the same information, just written in two different forms.

The curve:

$y^2=x^3-n^2x$

where $n=6$, looks like this:

![The elliptic curve y^2 = x^3 - n^2x with n = 6, showing the point (12,36)](/assets/desmos-n6.png)

The point $(12,36)$ lies on this curve, and because both coordinates are rational and $y\neq0$, it corresponds to a rational right-angled triangle with area $6$. In this case, the corresponding triangle is $(3,4,5)$.

However, the difficult part is that for a general value of $n$, it is hard to determine whether the curve:

$y^2=x^3-n^2x$

has a rational point with $y\neq0$. This is why the congruent number problem remains difficult even after being translated into an elliptic curve.

## Tunnell's theorem

Since it is difficult to directly decide whether the elliptic curve:

$y^2=x^3-n^2x$

has a rational point with $y\neq0$, mathematicians have developed other tests connected to elliptic curves. One important one is **Tunnell's theorem**, which gives a way to test whether a number is congruent by counting the integer solutions to certain equations. This is useful because it turns the problem into something finite that can be checked.

For a square-free positive integer $n$, Tunnell's theorem gives the following tests. For a general positive integer, we can first remove square factors, because multiplying a congruent number by a square factor preserves congruence.

For even $n$, define:

$h(n)=\lvert\{(x,y,z)\in\mathbb{Z}^3:x^2+4y^2+8z^2=\frac{n}{2}\}\rvert$

and:

$k(n)=\lvert\{(x,y,z)\in\mathbb{Z}^3:x^2+4y^2+32z^2=\frac{n}{2}\}\rvert$

Here, the vertical bars mean “the number of”, so $h(n)$ and $k(n)$ count how many integer triples $(x,y,z)$ satisfy the equation.

For even $n$, the test is:

$h(n)=2k(n)$

For odd $n$, define:

$A(n)=\lvert\{(x,y,z)\in\mathbb{Z}^3:2x^2+y^2+8z^2=n\}\rvert$

and:

$B(n)=\lvert\{(x,y,z)\in\mathbb{Z}^3:2x^2+y^2+32z^2=n\}\rvert$

For odd $n$, the test is:

$A(n)=2B(n)$

The important detail is that Tunnell's theorem is fully reliable in one direction: if the equality fails, then the number is definitely not congruent. If the equality holds, then the number is congruent assuming the Birch and Swinnerton-Dyer conjecture, usually shortened to BSD.

Here is $n=2$ as an example.

$2$ is even, so we use the even Tunnell test formula:

$h(2)=\lvert\{(x,y,z)\in\mathbb{Z}^3:x^2+4y^2+8z^2=1\}\rvert$

and:

$k(2)=\lvert\{(x,y,z)\in\mathbb{Z}^3:x^2+4y^2+32z^2=1\}\rvert$

Since the right side is $1$, the only possible solutions are:

$(x,y,z)=(1,0,0),(-1,0,0)$

So:

$h(2)=2$

and:

$k(2)=2$

For even $n$, Tunnell's test requires:

$h(n)=2k(n)$

But for $n=2$:

$h(2)=2$

and:

$2k(2)=2(2)=4$

So:

$h(2)\neq2k(2)$

Therefore, $2$ is not congruent.

Tunnell's theorem is good because with earlier methods, like algorithms, we could only provide examples of congruent numbers, but with Tunnell's theorem, we can use it to prove whether a certain number is congruent or not. Tunnell's theorem gives a finite test by reducing the question to counting integer solutions.

However, the full use of Tunnell's theorem depends on the Birch and Swinnerton-Dyer conjecture, usually shortened to BSD.

BSD is a major unsolved conjecture about elliptic curves. It predicts a deep connection between the rational points on an elliptic curve and a special function attached to the curve, called its $L$-function. This matters for the congruent number problem because deciding whether $n$ is congruent is equivalent to deciding whether the elliptic curve:

$y^2=x^3-n^2x$

has a rational point with $y\neq0$. Tunnell's theorem gives a practical test for congruent numbers, but using it as a complete test depends on BSD.

Therefore, the congruent number problem is still not fully solved because its full solution is connected to an unsolved problem about elliptic curves, and until BSD is proven, the congruent number problem remains unsolved.

To end it on a rather fun note, here is a fact about BSD: the BSD conjecture is one of the seven Clay Millennium Problems, and if you solve it, you win \$1,000,000 and mathematical fame.

## Conclusion

In conclusion, this post explored how the congruent number problem can quickly evolve from a simple question about the areas of right-angled triangles to a much deeper mathematical problem, requiring multiple complex methods with a lot of maths behind them.

At first, I used Pythagorean triples and scaling to show how examples of congruent numbers can be produced, such as $5$, $6$, and $45$. This led to an algorithm for finding congruent numbers by generating Pythagorean triples, calculating their areas, and removing square factors if there were any. However, this method has clear limitations. For example, it can find examples, but it does not provide a reliable way to decide whether any chosen number is congruent, since some numbers may only appear after a very long search, such as $53$.

The elliptic curve approach gave a much deeper way to study the problem since we could now treat the congruent number problem as a question of what are the rational points of the curve:

$y^2=x^3-n^2x$

where $y\neq0$. However, this also showed why the problem remains difficult, since determining whether a curve has such a rational point can itself be very hard.

Tunnell's theorem gives a more practical method by reducing the problem to counting integer solutions to certain equations. However, its full use still depends on the Birch and Swinnerton-Dyer conjecture. Since BSD remains unproven, the congruent number problem still remains unsolved, over a thousand years later.

For me, the most interesting part of the congruent number problem is how quickly it moves from a question about triangle areas to some of the deepest unsolved ideas in modern mathematics.

## Sources

- Keith Conrad, *The Congruent Number Problem*, University of Connecticut.
- UCL Mathematics Masterclass slideshow on *The Congruent Number Problem* by Dr Niki Kalaydzhieva.
- American Institute of Mathematics, *The first 1 trillion coefficients of the congruent number curve*.
- Desmos Graphing Calculator.
- Wikipedia, *Birch and Swinnerton-Dyer conjecture*.
- John Coates, *The Congruent Number Problem*, University of Cambridge.
- Leonardo Tang, *Congruent Number Problem*, YouTube.
