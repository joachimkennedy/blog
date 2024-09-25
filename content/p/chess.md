---
title: "Heuristics In Chess"
date: 2021-12-31T06:40:32-08:00
tags: ['2021', 'thoughts']
---

To me, one of the most fascinating aspects of Chess is the relative value of the pieces.
From the first Chess class I remember taking (probably around Kindergarten or First Grade), I learned that a Pawn is worth 1 point of material; Knights and Bishops are worth 3 each; Rooks are worth 5; and the powerful Queen is worth 9.
Along with the ways the pieces move, their relative values are among the first things beginners learn about Chess and perhaps one of the few things nonplayers know about the game.
Whenever I walk up to a board in the middle of a game, I count the material balance even before evaluating the position.
The most popular chess websites display the material balance to the players as the game is going on.
The values of the pieces feel so viscerally *real*.

And yet, the material balance has virtually no **direct** impact on the outcome of the game.
Sure, the player with more material will generally have a better time of it, but even at the highest levels, it sometimes happens that one player will sacrifice material for a winning attack.
Even if one player has their whole army, as long as the other player has even a point of material, there remains the possibility, however unlikely, that they can win by checkmate.

The whole business of the pieces having point values is simply a heuristic to guide players as to which trades are favorable for them.
Although piece values may be the simplest and most accessible example, there are no shortage of heuristics in the game of Chess.
Beyond Material, the most commonly cited categories of heuristics are King Safety, Space, Pawn Structure, and Piece Activity and Coordination.
Generally the player with the safer King who controls more squares on the board and has more stable pawn chains is considered to have a better position.
Perhaps it would be clearer to mention what *isn't* Heuristic.

# Calculation

When looking at a Chess position, there are generally two ways to evaluate it. We've discussed Heuristics, but there is also the Calculation.
This is probably what most people think Chess is all about, but to give an example, imagine a puzzle in which White is one move away from checkmating Black.
Since that move would win the game for White, it would be fair to call it their best move.
Now step back to a two-move puzzle.
Now White plays a move, Black has a chance to respond, and White mates on their second move.
Perhaps Black has multiple options after White's first move, but no matter what, White will have a checkmate to play on their second move.
This position would be considered winning for White because, even though White could miss the sequence and lose later on, with best play, the game should result in White winning.

Said another way, Calculation is what you do when you say, "If I do this, they'll do that. etc."
This usually involves branching paths and crucially, it's difficult to do to great depth, even for computers.
It's just a hard computation.

Of course, in most positions, it's impossible to calculate to a forced checkmate.
This is where Heuristics come back in.
Rather than calculate to checkmate, most of the time, players are trying to calculate to better Pawn Structure or better Piece Activity or less Material for their opponent.

# Why Bullet Chess is Easy

I hope I'm not stepping on Kahneman and Tversky's toes by talking about Heuristics and Calculation, but most people, even most Chess players, overemphasize Calculation and underemphasize Heuristics.
I stumbled upon this dichotomy first through bullet chess.
More precisely, my experience telling people that I like to play 1 minute chess to relax and turn off my brain.
When I express this, I get looks of shock and disbelief, especially from other avid players.
It seems that most people imagine that in bullet chess, you perform the same calculations you would in a longer game, but faster.
Instead, at least in my experience, I calculate less often and less deeply.

Of course I'm not very good, but even when I watch higher rated players commentate their own bullet tournaments, they rarely seem to mention calculations longer than about 4-5 moves which would be nothing in a longer game.
Moreover, they often say things like, "My Bishop belongs over there." or "My Knight wants to be here." which says to me that they are using heuristics about where their pieces look active, harmonious, and safe.

I have a fun thought experiment that elucidates the importance of Heuristics as well.
I imagine that I got to play a game against Magnus Carlsen, the current World Chess Champion.
In this game, I can control time such that I have a day to think about my moves, and Magnus has an hour to think of his.
I think I'd still lose.
Even if I got weeks per move.
That is calculation is not the (only) limiting factor keeping me from being as good at chess as Magnus Carlsen.
Even if I could calculate as well as him, I couldn't beat him.
Even if I could avoid threats and get to the positions I wanted safely, those positions probably wouldn't even be favorable for me simply because I would still be worse at evaluating my Piece Activity and Coordination and Pawn Structure as well as him.

It's interesting that it's not so clear how you improve your Chess Heuristics.
If you want to improve at Calculation, you can do lots of puzzles or read books with Chess notation and visualize the position.
You can get good feedback on your calculations as well because if you make a mistake, it becomes obvious when what you thought would happen doesn't happen.
But with Heuristics, it's very easy to think you're better in a losing position, and still win because your opponent played slightly inaccurately later on.
I suspect common practice says that the way to improve at Heuristics is to play a lot of games and that randomness will get evened out, but if you're even slightly delusional, it becomes very easy to fool yourself.
Much better is to go over your games with a coach and an engine.
An engine will give you the (roughly) objective evaluation of the position.
A coach can interpret and explain what is better or worse about your position in a way that you can remember and generalize to future games.
I wonder if you could create "Chess Heuristic Puzzles" where you try to guess the computer evaluation of a given position (with no clear tactics) and if that method of practice would yield positive results.

# A Tangent

Writing this post made me realize exactly what I dislike about one of my least favorite sayings, variations on "There's an exception to every rule." or even worse, "The exception that proves the rule."
First of all, it's obviously false, and kind of meaningless.
There are many rules with no exceptions like, "Primes are only divisible by 1 and themselves," and "No running on the pool deck."
If I'm not being purposely obtuse, I see people actually mean, "There's an exception to every rule *of thumb*."
But even this is not totally accurate.
Yes, sometimes heuristics don't work, but that doesn't mean there are exceptions.
It just means that all models are wrong.
