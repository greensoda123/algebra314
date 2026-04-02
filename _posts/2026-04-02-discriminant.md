---
layout: post
title: "Why Does the Discriminant Determine the Number of Roots?"
date: 2026-04-02
---

Consider a quadratic equation:

$$
ax^2 + bx + c = 0
$$

We are often told that the expression $b^2 - 4ac$ — known as the discriminant — determines how many real roots the equation has.

But why does this happen?

---

## The Key Observation

Using the quadratic formula:

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

we see that everything depends on the square root term

$$
\sqrt{b^2 - 4ac}.
$$

The nature of this square root determines the number of real solutions.

---

## Case 1: $b^2 - 4ac > 0$

If the discriminant is positive, then $\sqrt{b^2 - 4ac}$ is a real, non-zero number.

This means the $\pm$ sign gives two different values, so the quadratic has **two distinct real roots**.

---

## Case 2: $b^2 - 4ac = 0$

If the discriminant is zero, then

$$
\sqrt{b^2 - 4ac} = 0.
$$

So the formula becomes

$$
x = \frac{-b}{2a}.
$$

Both values collapse into one, so the quadratic has **one repeated real root**.

---

## Case 3: $b^2 - 4ac < 0$

If the discriminant is negative, then $\sqrt{b^2 - 4ac}$ is not a real number.

So the quadratic has **no real roots**.

---

## A Graphical Interpretation

Now consider the graph

$$
y = ax^2 + bx + c.
$$

The roots of the quadratic are exactly the points where the graph meets the $x$-axis.

- If $b^2 - 4ac > 0$, the graph crosses the $x$-axis twice.
- If $b^2 - 4ac = 0$, the graph just touches the $x$-axis once.
- If $b^2 - 4ac < 0$, the graph does not meet the $x$-axis at all.

So the discriminant determines how many times the graph intersects the $x$-axis, which is why it determines how many real roots there are.

---

## Conclusion

The discriminant is not just a number to calculate mechanically. It controls the square root term in the quadratic formula, and that in turn determines whether the equation has two, one, or no real roots.
