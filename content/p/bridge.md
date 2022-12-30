---
title: "The Bridge Problem"
date: 2022-10-02T08:44:41-08:00
---

# Preamble

It would be ridiculous to move a blog to a static site generator after not updating it for 2 months, right?
Even if after posting one more blog post, it might not be justifiable.
The way I figure, the faster way to justify moving this blog to a static site generator is to write a post with some math that could really benefit from thoughtful formatting and maybe a couple useful diagrams.
By first writing this lazy, ugly, nigh unreadable text-only version, I am justifying fixing it at a later date.
If all goes to plan, it will be so hard for me to live with this, that I'll get around to updating the site all the faster.

---

# The Problem

I first encountered a variant of this problem on coolmathgames when I was a stupid kid and was recently reminded of it by my friend's version:

Four friends are out walking at night sharing one flashlight among them when the come upon a long, narrow, rickety wooden bridge over a gaping crevasse.
At most two of them can cross together at once.
The people crossing the bridge must carry the flashlight.
(Maybe there are no handrails on the bridge.)
(Don't worry about the people waiting in the dark while others are crossing.
Let's just say there aren't any feral animals around.
In fact, if it makes you feel better, we can pretend they're crawling through a long, narrow tunnel during the day.)
It takes each friend a different length of time to cross the bridge.
In speed (and, coincidentally, increasing shoe size and alphabetical by first name) order, they can cross in 1, 2, 5, and 10 minutes.
(Don't worry about how they know this ahead of time.
They probably timed it during the day.)
As usual, they try to walk as quickly as possible without leaving anyone behind (even Dave and his ridiculous clown shoes).
That is, when two people cross the bridge together, they take the pace of the slower walker.
What is the fastest they can cross the bridge?
(Wouldn't it have been faster if they just tried something instead of standing here arguing over the "optimal" method?)

I'll wait to jump into the solution and my reasoning.
In the meantime, I'm starting to believe that my purpose in life is to solve these little puzzles (among other things I'm sure), so please send me any juicy ones you know (unless it's about balancing counterfeit coins.
I'm still working on that one.)
Ok. Here's a hint if you want it.
The fastest method takes 17 minutes.

---

# The Solution

This is how I solved it.
The obvious and naive method would be to have the fastest person escort each of the others across the bridge and carry the flashlight back.
For example: 1 and 10 cross; 1 returns; 1 and 5 cross; 1 returns; 1 and 2 cross.
This method takes 10 + 1 + 5 + 1 + 2 = 19 minutes.
Since the naive answer is often right in math but rarely in puzzles, there's probably a faster way to do it.
(At this point, my friend told me 17 was the best you could do).
It feels more efficient for 10 and 5 to cross together, but obviously neither of them should carry the flashlight back.
Those conditions are restrictive enough that I could say: 1 and 2 cross; 1 returns; 5 and 10 cross; 2 returns; 1 and 2 cross whereupon my friend told me that was correct.
(This is 2 + 1 + 10 + 2 + 2 = 17).

As far as puzzles go I find it pretty unsatisfying because it's possible to get the correct answer without knowing for certain that it is.
You could brute force all the combinations to see verify that it is optimal, but what about groups with other walking speeds?
It's not really clear what's going on.
Is this method always better?

---

# More Bridge Fun

Here is my rigor-is-for-the-corpses reasoning about the fun parts of the problem.
First, we can generalize the times-to-cross as 1 &le; a &le; b &le; c.
(Note the fastest person may not cross in 1 minute, but we can always scale everything so that they do.)
It's always nice to have even loose, gratuitous bounds.
Since the slowest person must cross, the answer must be at least c.
For the upper bound, we can just use the naive solution since it's easy to calculate (2 + a + b + c in the general case).
Compare this to our alternate method, 1 + 3a + c.
They are equally good when b = 2a - 1. (e.g. 1, 3, 5, 10).
This kind of makes sense.
The tradeoff is that we can avoid the second slowest person contributing any additional time if the second faster person takes more trips.
(Interestingly, the fastest and slowest people don't matter).

This become more apparent if we take an extreme example.
Imagine we exchange the two slowest friends with a turtle and a snail that can cross in 99 and 100 minutes respectively (and still need the flashlight).
It's pretty obvious that it's best for them to travel together.
The difference is 100 + 1 + 99 + 1 + 2 = 203 vs. 2 + 1 + 100 + 2 + 2 = 107. Much faster. Not even close. Would not make an exciting race. You could start *The Seventh Seal* when the first team finished and be done when the second team finally finished. Or *When Harry Met Sally* if you're in the mood for something lighter.

Ok I know what you're thinking.
That's all great, but what if there are more than 4 people?
Let me counter with an easier question.
What if there are fewer than 4 people?
If there are 0, 1, or 2 people, the problem is very easy.
Zero people take no time to cross a bridge. Very fast.
One person crosses in 1 arbitrarily scaled fake minute.
Two people (1 and a) cross in *a* time.
Three people take more steps, but there still aren't really options.
They (1, a, and b) cross in *1 + a + b* time.

Now that I'm done putting it off, I'm not sure the best way to handle more than 4 people.
But that won't stop me from saying what I think it is.
Please correct me if I'm wrong, but I think you can think of the problem as successively getting the slowest two people across (using whichever method discussed above is faster).
I know the coolmathgames version had more than 4 people, but since flash games died, there's tragically no way for me to check my reasoning in a fun, interactive way.

---
