---
layout: post
title: The Binomial distribution
---

### Learning Statistics with ease

Statistics and Probability belong to the scariest words list of many students. I deeply understand, and therefore this blog is my dedication for any student who is like me, afraid of those "big words" and have no idea what the teacher is talking about some time or most of the time.

Today topic is **Binomial distribution**, and believe me, you want to know what is this and how can you use it.

**The Binomial distribution** is an important term in statistics and is widely applied in many aspects of life: predicting the probability (chance) a new line of drug works successful, whether Trump (or I should say a Republican candidate) will win the second election or chance a student passes this class and so on.

### Some examples:

First, to understand this, we start with an example of two lists: list x contains the subject a student took last semester and list y contains the time (hour: minute: second) each person finish a marathon. 

$x = [physics, math, literature]$

$y = [2:50:00,3:50:03,5:10:05,...]$

Since we can control the value taken in list x (a finite number of data) while value in list y can be any number within a certain range (from 2:02:57[^1] to 6:00:00[^2]), we say: All the value in list x is *discrete* (countable) and values in list y is *continuous* (uncountable). Only discrete value is used in **binomial distribution**.

Now let's imagine on a sunny day in Vancouver, you decide to buy a lottery ticket from Daily Lotto, which you will either win some money or not. For a month since that day, every morning you buy one ticket and hope to win. There are only two outcomes of this action, so the outcome is a discrete value. In this case, we consider winning money as a success (X) and not winning is a "failure" (Y).

Every morning, the chance of winning is equally the same, let's call it $p$.

$P(X) = p$ 

$P(Y) = 1 - p$

The probabilities of both outcomes' occurrence in this experiment is an example of **the binomial distribution**. 

### Definition and formula:

Looking at the term carefully can reveal some hints to its meaning. 

The prefix "bi" means two, and "binomial" means the sum of two things or consist of two terms. In order to be called "binomial", there are four conditions:

- There are a *specific number* of experiments. (in the example above, the number is 30)
- There are two and *only two possible outcomes* of each experiment. (winning or not)
- For each experiment, *the probability of each outcome's occurrence is the same*. (Since each day the Daily Lotto has a winner, the chance of winning a ticket does not increase when you buy another one the next day. In short, you have the same chance to win a lottery each time you buy a ticket)
- Each experiment is *independence* - it does not depend on the result of the previous experiment. (The fact that you bought a lottery ticket yesterday did not prevent or encourage you to buy another one today.)

In summary, **binomial distribution** is the discrete probability distribution of a number of time an expected outcome occurs with four conditions mentioned above. 

To calculate the probability of an expected outcome happens $x$ time in $n$ trials, we use this formula[^3]:

![](binom1.gif)



### Application of binomial distribution

Here are some simple real-world problems that can be solved by using **binomial distribution**:

1. In country A, the malnutrition rate in children under 5 years old is 20%. If we check randomly 10 boys and girls under 5 years old, what is the probability of having 2 malnutrition children?

   The expected outcome is: finding a malnutrition kid. 

   With $n = 10, x = 2, p = 0.2$, the probability of having 2 malnutrition children is:

   $P(X=2) = \frac{n!}{x!(n-x)!}  p^x q^{n-x}$

   $P(X=2) = \frac{10!}{2!(10-2)!}  0.2^2 0.8^{10-2}$

   $P(X=2) = 0.3$

2. Every year, the IRS estimates that 5% of high net worth individual will try to cheat the government in their tax return. If a random 100 tax returns is being audited by the IRS, what is the probability of finding 5 cheaters? [^4]

   The expected outcome is: finding a big shot that does not want to pay tax.

   With $n = 100, x = 5, p = 0.05 $, the probability of having 5 fraudulent tax returns is:

   $P(X=5) = \frac{n!}{x!(n-x)!}  p^x q^{n-x}$

   $P(X=5) = \frac{100!}{5!(95)!}  0.05^5 0.95^95$

   $P(X = 5) = 0.18$

   On the other hand, we can calculate the probability of checking randomly 200 tax return and find no fraud at all:

    $n = 200, x = 0, p = 0.05 $

   $P(X=0) = \frac{n!}{x!(n-x)!}  p^x q^{n-x}$

   $P(X=0) = \frac{200!}{0!(200)!}  0.05^0 0.95^{200}$

   $P(X = 0) = 0.000035$ (really small)

   The result of these tests is a reasonable number of tax return that IRS should audit to find out a fraudulent tax  return without checking every single one. 

NOTE: the **binomial distribution** can also be used to estimate the probability of at least or at most $x$ times an expected event happens.



[^1]: Number is taken from IAAF: https://www.iaaf.org/records/toplists/road-running/marathon/outdoor/men/senior
[^2]: The limit time for a marathon varies from 5 to 6 hours depends on the place.
[^3]: More explanation and this picture can be found in this source: [Mathnstuff website]( http://www.mathnstuff.com/math/spoken/here/2class/90/binom3.htm#ans)
[^4]: This example is rewritten in a simple form, the original example can be found in the Coursera course of Rice University: Basic Data Descriptors, Statistical Distributions, and Application to Business Decisions

