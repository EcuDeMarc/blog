---
title: "Money Network"
date: 2021-08-15T10:18:43+01:00
---

Money is best thought as a network of credit/debit relationships.

A relatively simple money network is shown in the image below.

![Example money network](/money_network.png)

In the image, we can see four actors (A,B,C,D).

Each actor has at least one relationship, denoted by an arrow, with another actor.

For example, taking the arrow going from actor A to actor B, we can see that B owes 100 to A. Looking at the arrow from D to A we can see that D has a credit claim of 10 on A. Finally, looking at the arrow going from C to A, one can conclude that A has incurred a debt of 25 towards C.

## Balance sheets

By looking at the credit/debit relationships visualized in the image above, one can compute a balance sheet for each one of the actors in the network.

### Actor A

| Credit         | Debit        |
| :------------- | :----------- |
| 100            | 35           |

### Actor B

| Credit         | Debit        |
| :------------- | :----------- |
| 50             | 100          |

### Actor C

| Credit         | Debit        |
| :------------- | :----------- |
| 25             | 50           |

### Actor D

| Credit         | Debit        |
| :------------- | :----------- |
| 10             | 0            |


## The sum of credits and debits have to cancel out

If you take all of the balance sheets of any money network and sum up all the credits and subtract the sum of all the debits you should always get a result of zero. In other words, in any money network, the sum of the credits should always be equal to the sum of all of the debits. You cannot have a situation in which the credits exceed the debits and vice versa.

We can verify whether this property is respected in the example money network we show in this post, by summing up all of the credits.

```
100 + 50 + 25 + 10 = 185
```

We can then sum up all of the debits.

```
35 + 100 + 50 + 0 = 185
```

As we can see, in our example, the sum of credits is equal to the sum of debits. We can say that this example money network respects the property where the sum of the credits and of the debits cancel out.

## Aggregate vs. detailed analysis

Altough the credits and debits have to cancel out in aggregate in any money network, we can see that this may not be true at an actor level.

Indeed, there are some actors that have many credits and very few debits (e.g. actor A and C) and actors that have many debits and few credits (e.g. actor B, C).

Thus, from this one can conclude that an analysis at an aggregate level is not that informative and a more detailed analysis of the network is of more use.

## Equity

The concept of equity is defined as follows:

```
equity = credits - debits
```
In short, equity stands for the value of credits in excess of the value of debits. Equity is what the actor would end up having in credits after the extinction of all the debits.

By using the above definition, we can easily calculate the equity for each one of the actors in our example money network.

| Actor          | Equity       |
| :------------- | :----------- |
| A              | 65           |
| B              | -50          |
| C              | -25          |
| D              | 10           |

One can see that two actors (A, D) have positive equity and that two actors (B, C) have negative equity.

By the property, described above, that the sum of credits and debits have to cancel out, we can also say that the sum of the equity in any money network has to sum up to exactly zero. We can verify that this latter property is respected in the example money network we show in this post by performing the following calculation.

```
65 - 50 - 25 + 10 = 0
```

We can indeed conclude that the equity of the example money network shown in this post sums up to zero as expected.

## Conclusion

From the above, we can see that no equity can ever be created in any money network at an aggregate level.

Thus, what really matters is the distribution of the equity in the money network.
