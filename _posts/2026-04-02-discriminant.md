---
layout: post
title: "Why Does the Discriminant Determine the Number of Roots?"
date: 2026-04-02
---

Consider a quadratic equation:

$$
ax^2 + bx + c = 0
$$

We are often told that the expression

$$
b^2 - 4ac
$$

— known as the *discriminant* — determines how many solutions the equation has.

But why does this happen?

---

## The Key Observation

Using the quadratic formula:

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

we see that everything depends on the square root:

$$
\sqrt{b^2 - 4ac}
$$

The nature of this square root determines the number of real solutions.

---

## Case 1: \( b^2 - 4ac > 0 \)

If the discriminant is positive, then:

- \( \sqrt{b^2 - 4ac} \) is a real, non-zero number
- The \( \pm \) produces two different values

So we obtain **two distinct real roots**.

---

## Case 2: \( b^2 - 4ac = 0 \)

If the discriminant is zero, then:

$$
\sqrt{b^2 - 4ac} = 0
$$

So the formula becomes:

$$
x = \frac{-b}{2a}
$$

Both solutions collapse into one.

This gives **one repeated root**.

---

## Case 3: \( b^2 - 4ac < 0 \)

If the discriminant is negative, then:

- \( \sqrt{b^2 - 4ac} \) is not real
- The solutions involve complex numbers

So there are **no real roots**.

---

## A Graphical Interpretation

Consider the graph of:

$$
y = ax^2 + bx + c
$$

- If \( b^2 - 4ac > 0 \): the graph crosses the x-axis twice  
- If \( b^2 - 4ac = 0 \): the graph touches the x-axis once  
- If \( b^2 - 4ac < 0 \): the graph does not meet the x-axis  

So the discriminant determines how many times the graph intersects the x-axis — which is exactly the number of real solutions.

---

## A Deeper Insight

The discriminant measures whether the square root term in the quadratic formula introduces *variation*.

- If it is positive, the \( \pm \) creates two distinct values  
- If it is zero, the variation disappears  
- If it is negative, the solutions leave the real number system  

In this sense, the discriminant encodes the entire behaviour of the solutions.

---

## Conclusion

The discriminant is not just a value to compute — it reveals the structure of a quadratic equation.

By controlling the square root in the quadratic formula, it determines whether we obtain two, one, or no real solutions.
