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

Now that $S_1$ has been assigned the value $\frac12$, we can try to find $S_2$ using some clever addition. Adding a second copy of $S_2$, shifted one place to the right, gives:

<div style="overflow-x: auto; margin: 1.5rem 0;">
<table style="margin: 0 auto; width: auto; border-collapse: collapse; border: none; background: transparent;">
  <tbody>
    <tr>
      <td style="padding: 0.2rem 0.55rem; text-align: right; border: none; background: transparent; white-space: nowrap;">$S_2$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$=$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$1$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$-2$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$+3$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$-4$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$+5$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent; white-space: nowrap;">$-6+\cdots$</td>
    </tr>
    <tr>
      <td style="padding: 0.2rem 0.55rem; text-align: right; border: none; background: transparent; white-space: nowrap;">$+\,S_2$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$=$</td>
      <td style="padding: 0.2rem 0.55rem; border: none; background: transparent;"></td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$1$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$-2$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$+3$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$-4$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent; white-space: nowrap;">$+5-\cdots$</td>
    </tr>
    <tr>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: right; border: none; border-top: 1px solid currentColor; background: transparent; white-space: nowrap;">$2S_2$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$=$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$1$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$-1$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$+1$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$-1$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$+1$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent; white-space: nowrap;">$-1+\cdots$</td>
    </tr>
  </tbody>
</table>
</div>

Therefore,

$2S_2=S_1$

Since $S_1=\frac12$,

$2S_2=\frac12$

$S_2=\frac14$

Finally, we can use $S_2$ to find a value for the target series:

<div style="overflow-x: auto; margin: 1.5rem 0;">
<table style="margin: 0 auto; width: auto; border-collapse: collapse; border: none; background: transparent;">
  <tbody>
    <tr>
      <td style="padding: 0.2rem 0.55rem; text-align: right; border: none; background: transparent; white-space: nowrap;">$S$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$=$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$1$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$+2$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$+3$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$+4$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$+5$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent; white-space: nowrap;">$+6+\cdots$</td>
    </tr>

    <tr>
      <td style="padding: 0.2rem 0.55rem; text-align: right; border: none; background: transparent; white-space: nowrap;">$-\,S_2$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$=$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$1$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$-2$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$+3$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$-4$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent;">$+5$</td>
      <td style="padding: 0.2rem 0.55rem; text-align: center; border: none; background: transparent; white-space: nowrap;">$-6+\cdots$</td>
    </tr>

    <tr>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: right; border: none; border-top: 1px solid currentColor; background: transparent; white-space: nowrap;">$S-S_2$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$=$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$0$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$+4$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$+0$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$+8$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent;">$+0$</td>
      <td style="padding: 0.3rem 0.55rem 0.2rem; text-align: center; border: none; border-top: 1px solid currentColor; background: transparent; white-space: nowrap;">$+12+\cdots$</td>
    </tr>
  </tbody>
</table>
</div>

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

This series only converges when $\lvert x\rvert<1$.

For example, when $x=\frac12$,

$1+\frac12+\frac14+\frac18+\cdots=2$

and

$\frac1{1-\frac12}=2$

The series and the formula agree.

However, the expression

$\frac1{1-x}$

also has values outside the range $\lvert x\rvert<1$. If $x=2$, then

$\frac1{1-2}=-1$

This does **not** mean that

$1+2+4+8+\cdots=-1$

The series still diverges. It only means that the function represented by the geometric series inside its region of convergence continues to exist outside that region.

The same basic distinction applies to the zeta function. The series

$\sum_{n=1}^{\infty}\frac1{n^s}$

does not converge at $s=-1$, but the function that it defines for $\mathrm{Re}(s)>1$ can be analytically continued to $s=-1$.

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

which converges when $\lvert x\rvert<1$.

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

In [blackpenredpen's Ramanujan summation video](https://www.youtube.com/watch?v=U_g_OZLt4OU), the regularised sum is found using a formula closely connected to the [Abel--Plana formula](https://dlmf.nist.gov/2.10).

The video places an $R$ above the equals sign. Since that notation does not render properly on this website, I will instead use $R(\cdot)$ to mean the Ramanujan-regularised value.

The formula can then be written as:

$R\left(\frac{f(0)}2+\sum_{n=1}^{\infty}f(n)\right)=i\int_0^\infty\frac{f(it)-f(-it)}{e^{2\pi t}-1}\,dt$

For

$1+2+3+4+\cdots$

we let

$f(x)=x$

Since $f(0)=0$,

$R(1+2+3+4+\cdots)=i\int_0^\infty\frac{it-(-it)}{e^{2\pi t}-1}\,dt$

As

$it-(-it)=2it$

and

$i(2it)=-2t$

we get

$R(1+2+3+4+\cdots)=-2\int_0^\infty\frac{t}{e^{2\pi t}-1}\,dt$

Now use the substitution

$u=2\pi t$

This gives

$t=\frac{u}{2\pi}$

and

$dt=\frac{du}{2\pi}$

Therefore,

$-2\int_0^\infty\frac{t}{e^{2\pi t}-1}\,dt=-\frac1{2\pi^2}\int_0^\infty\frac{u}{e^u-1}\,du$

There is a standard connection between this integral, the gamma function and the zeta function:

$\int_0^\infty\frac{u^{s-1}}{e^u-1}\,du=\Gamma(s)\zeta(s)$

For $s=2$,

$\int_0^\infty\frac{u}{e^u-1}\,du=\Gamma(2)\zeta(2)$

The gamma function extends the factorial, with

$\Gamma(n)=(n-1)!$

so

$\Gamma(2)=1$

We also know that

$\zeta(2)=\frac{\pi^2}{6}$

Therefore,

$\int_0^\infty\frac{u}{e^u-1}\,du=\frac{\pi^2}{6}$

Substituting this into the earlier result gives

$R(1+2+3+4+\cdots)=-\frac1{2\pi^2}\times\frac{\pi^2}{6}$

and therefore

$R(1+2+3+4+\cdots)=-\frac1{12}$

Again, this does not mean that the ordinary series converges to $-\frac1{12}$. The $R$ shows that a different method of summation is being used.

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

or, using the notation defined earlier,

$R(1+2+3+4+\cdots)=-\frac1{12}$

The ordinary series diverges, but $-\frac1{12}$ is a regularised value that can still be associated with it.
