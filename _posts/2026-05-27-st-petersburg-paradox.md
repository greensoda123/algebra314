# The Game Worth an Infinite Fortune (That Nobody Would Play)

## The St. Petersburg Paradox and what it reveals about the limits of rational thought

Imagine I offer you a deal.

We flip a fair coin, over and over, until it lands heads. If heads comes up on the very first flip, I hand you £2. If it takes two flips, £4. Three flips, £8. Every time the streak continues, the payout doubles. You could walk away with £2, or £1,024, or, if you're extraordinarily lucky, more money than exists on Earth.

The question is simple: **how much would you pay to play?**

Take a moment. Actually think about it. Most people land somewhere between £5 and £25. A few bold types go up to £50. Almost nobody says more than £100, and the rare person who says £1,000 is usually showing off rather than reasoning carefully.

Here's the problem. According to the mathematics of expected value, the framework that underpins modern economics, insurance, and most of how we think about rational decision-making, your answer should be every penny you own. You should sell your house, liquidate your savings, and beg, borrow, or steal the rest. The correct price for this game, by the numbers, is infinity.

This is the **St. Petersburg Paradox**. It is either a devastating flaw in probability theory, a profound insight into human psychology, or both. Mathematicians and economists have been arguing about it since 1713, and the argument is still not fully settled.

## The Maths, Done Properly

To understand why the game is worth infinite money, you need to understand **expected value**. It's a simple idea: for any gamble, multiply each possible outcome by its probability, then add them all up. The result is the average payout you'd get if you played the game a huge number of times.

Take a simpler example first. A fair die. Roll it and you win whatever number comes up, in pounds. The expected value is:

$$
\left(\frac{1}{6} \times £1\right)
+
\left(\frac{1}{6} \times £2\right)
+
\left(\frac{1}{6} \times £3\right)
+
\left(\frac{1}{6} \times £4\right)
+
\left(\frac{1}{6} \times £5\right)
+
\left(\frac{1}{6} \times £6\right)
=
£3.50
$$

That's a clean, finite number. You'd happily pay £2 to play, feel ripped off paying £4, and call it roughly fair at £3.50. Expected value works perfectly.

Now back to the coin game. The probability of heads coming up on flip number $n$ is $\left(\frac{1}{2}\right)^n$. The payout for that outcome is $£2^n$. So the expected value contribution of each possible outcome is:

$$
\left(\frac{1}{2}\right)^n \times £2^n = £1
$$

Every single outcome, no matter how unlikely, contributes exactly £1 to the expected value. And there are infinitely many possible outcomes.

$$
£1 + £1 + £1 + £1 + \cdots = \infty
$$

That third row is where the paradox lives. Every column is £1 and the columns never stop:

$$
\renewcommand{\arraystretch}{1.4}
\begin{array}{c|ccccccc}
x & 2 & 4 & 8 & 16 & \cdots & 2^n & \cdots \\
\hline
P(X = x) & \dfrac{1}{2} & \dfrac{1}{4} & \dfrac{1}{8} & \dfrac{1}{16} & \cdots & \dfrac{1}{2^n} & \cdots \\
\hline
xP(X = x) & 1 & 1 & 1 & 1 & \cdots & 1 & \cdots
\end{array}
$$

This is not a trick. The maths is correct. The formula gives the right answer: infinity. The paradox is that this answer is completely useless.

## Why Your Gut Is Screaming "No"

Your instinct not to pay more than £20 or so isn't irrationality. It's your brain quietly running a more sophisticated calculation than the textbook formula.

Think about what actually happens when you play. Half the time, you get £2. A quarter of the time, £4. One in eight times, £8. By the time you're looking at a payout of £1,024, the probability is roughly one in five hundred. A payout of £1 million requires about 19 consecutive tails, a one in half-a-million shot. The astronomical payouts that push the expected value toward infinity are so vanishingly rare that you'd almost certainly never see them in a lifetime of playing.

In a very real sense, the expected value is being held hostage by outcomes that will never happen to you. The formula counts them anyway, and counts them heavily, because the payouts grow just as fast as the probabilities shrink. Mathematically they perfectly cancel out. In reality, you only play the game once, and you're almost certainly going home with less than £32.

This gap, between what the maths says in aggregate and what actually happens to any individual player, is at the heart of the paradox.

## A Brief History of People Trying to Fix This

The problem was first posed by Nicolas Bernoulli in a letter to Pierre Rémond de Montmort in 1713. It sat around causing headaches for about twenty-five years before Nicolas's cousin Daniel Bernoulli published what became the most famous proposed solution in 1738.

### Daniel Bernoulli and the Diminishing Value of Money

Daniel's insight was elegant: the formula for expected value treats all money as equal, but money isn't equal. The first £100 you earn in a month matters enormously; it feeds you. The hundred-thousandth pound matters far less. Wealth has **diminishing marginal utility**, meaning each additional pound you gain is worth slightly less to you than the previous one.

This isn't a psychological quirk. It's a genuine feature of how value works. Imagine you have £1,000 in your bank account. Someone offers you a coin flip: heads you win £1,000, tails you lose £1,000. The expected monetary value is zero; you'd end up with £2,000 or £0, averaging to your current £1,000. But almost no rational person would take this bet, because losing £1,000 when you only have £1,000 is catastrophic, while gaining £1,000 when you already have it is merely nice.

Bernoulli proposed replacing raw monetary value with **utility**, a measure of how much each pound actually matters to you, and suggested that utility grows logarithmically with wealth. Under this framework, the St. Petersburg game has a finite expected utility, which lines up with the modest amounts people are actually willing to pay.

It's a genuinely good solution, and it introduced ideas that are still central to economics today. But it has a problem.

You can construct a version of the St. Petersburg game where the payouts grow fast enough to overcome any logarithmic utility function. Instead of doubling, make the payout grow super-exponentially. Now the expected utility is infinite again, and Bernoulli's fix stops working. The paradox just moves to a different address.

### The Bounded Wealth Objection

A more pragmatic response: no casino in the world could actually pay out $£2^{50}$, let alone $£2^{1,000,000}$. If you cap the maximum payout at what any realistic counterparty could afford to pay, say, the GDP of the entire planet, the expected value becomes finite and quite modest.

This is a fair point. In any real-world version of the game, there is a ceiling. And once you introduce that ceiling, the theoretical paradox evaporates.

The problem with this fix is that it solves the wrong problem. The paradox is about the mathematics of expected value, not about casino regulations. We're asking whether expected value is the right framework for making decisions, and "well, you can't pay out infinity anyway" doesn't answer that question. It just sidesteps it.

### Risk Aversion and the Psychology of Losing

A third strand of thought comes from behavioural economics, particularly the work of Daniel Kahneman and Amos Tversky in the 1970s and 1980s. Their research showed that humans don't weight outcomes by probability in the linear way expected value theory assumes. We're systematically bad at reasoning about very small probabilities; we either ignore them entirely or dramatically overweight them.

We also feel losses more acutely than equivalent gains. Losing £100 feels roughly twice as bad as winning £100 feels good. This asymmetry, known as **loss aversion**, means we're naturally risk-averse in a way that can't be fully captured by utility theory alone.

Under **prospect theory**, the framework Kahneman and Tversky developed, the tiny probabilities of enormous St. Petersburg payouts get underweighted, and the certain cost of entry gets overweighted. The game looks like a bad deal because we're not wired to intuitively grasp what "one in a million chance of £1,048,576" actually means.

This is descriptively accurate; it explains how people actually behave. Whether it's normatively correct, whether we should behave this way, is a different and harder question.

### Rejecting Expected Value Altogether

The most radical response is to question whether expected value is the right tool for decisions like this at all. The economist Ole Peters has argued that expected value conflates two fundamentally different kinds of averages: the average across many people playing simultaneously, an **ensemble average**, and the average for one person playing repeatedly over time, a **time average**.

For the St. Petersburg game, these averages behave very differently. The expected value calculation is essentially asking: if a million people each played this game once, what's the average payout? Answer: enormous, dominated by the rare cases where someone hits a 20-flip streak.

But that's not your situation. You're one person, playing once, and your outcome is going to be somewhere in the very common lower range of results. Peters argues that **ergodicity**, whether ensemble averages and time averages coincide, is the missing piece that makes the paradox dissolve when accounted for properly.

This is genuinely interesting work, though it remains contested among economists. It suggests the problem isn't with human intuition but with the mathematical framework we're using to judge it.

## What Intuition Gets Right

Here's the thing. Every serious proposed solution to the St. Petersburg Paradox ends up agreeing with your gut feeling: the game is not worth infinite money. They just disagree about why.

Bernoulli says: because the utility of money diminishes.

The bounded-wealth crowd says: because infinite payouts don't exist.

Kahneman and Tversky say: because we systematically discount tiny probabilities.

Peters says: because expected value is asking the wrong question.

Your instinct to pay around £20 wasn't random. It was your brain, with no formal training in probability theory, somehow landing in the same ballpark as several centuries of academic effort. That's worth taking seriously.

The deeper lesson isn't that humans are bad at maths. It's that expected value, while a powerful and useful tool, captures only one aspect of what makes a decision good or bad. It ignores the shape of the distribution of outcomes, your personal financial situation, the one-shot nature of most real decisions, and the real-world constraints on any counterparty's ability to pay.

For routine decisions where outcomes are modest and roughly symmetric, expected value works brilliantly. For decisions involving extreme, rare, and potentially unbounded outcomes, think pandemic risk, catastrophic financial bets, or tail-risk insurance, it can actively mislead you.

## The Paradox That Keeps Giving

More than three hundred years after Nicolas Bernoulli first posed it, the St. Petersburg Paradox remains genuinely unresolved in the sense that matters: there is no single fix that economists and philosophers universally agree on. Different camps accept different solutions, and each solution exposes a different assumption buried in how we think about rationality.

That's actually what makes it such a good paradox. It isn't unsolvable in the way that Fermat's Last Theorem was once unsolvable; nobody doubts that the expected value is infinite. The paradox is that a correct mathematical result produces an obviously wrong practical conclusion, and every attempt to explain the gap reveals something new and interesting about the relationship between mathematics, money, and the way human minds actually work.

So: what would you pay to play?

If your answer is somewhere between £10 and £30, you're in excellent company. You're also, depending on which economist you ask, either irrationally risk-averse or displaying a sophisticated implicit grasp of ergodicity, diminishing marginal utility, and the practical limits of ensemble reasoning.

The game is worth an infinite fortune. You'd pay twenty quid. Both of these things are, in their own way, correct.
