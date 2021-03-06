# Beginnings, the long list, the short list (Friday, 10 April 2020, 14:33PM)

So COVID-19 is still The Big Thing out there and it seems like the best response is to make work that is in some sense "easy" to put together and think through. Right now the line of least resistance for me still seems to be chess, and so I figured I'd just immediately start on some new chess variations since I've been thinking about it lately anyway.

Presumably this is all because I've been _playing_ a lot of chess for the last while on lichess.org.

## The long list

Anyway, I have a set of variations in mind. Let me paste in the thoughts I had listed in Things for the last while:

- COMEDY - Laughtrack on certain moves (can just be random though)
- CHEST - Upgrade/loot boxes that maybe convert your piece to a better piece, give you an extra pawn, etc. Have to decide if it's worth going out of your way to get them?
- ESP/TELEKINESIS/GELLER - Instruction to move your piece with your mind
- 4'33" - Just a chess set and you can't/don't play, you just sit and think about chess and the chess-like nature of the world around you, and the game lasts (with time control) for 4:33)
- MEMORY - Pieces all display, then flip over. You have to choose a square and a destination, then the first square flips to show if there's a legal piece, and the second square flips to show if it's a legal destination? What about pieces in between? Kind of like this idea? About maintaining a memory of the board, but also the weird memory game? The more drastic version is just the board and you make moves and are only told if it was legal or not, and if illegal you lose your turn? So a huge advantage to playing legal moves and maintaining your memory of the board? Maybe it could be a "special move" to reveal a square instead of moving one? There's something to this one. Especially like the idea of squares rotating away the piece on them.
- HALVES - You move pieces by halves (use transparency), so on any turn you make two moves, but you can move different halves. (Except the king as always, because you can't have multiple kings on the board). Would have to understand captures. (Can a half-piece capture a whole piece? I guess the capture just does as much "damage" as there are fractions of a piece in that position?)
- IMMORTAL - You have to make the pieces in the immortal game or you get a takeback and a "Wait... that's not what happened"... (and you're the loser)
- PACIFIST - Check/checkmate but no captures? I guess it just gets all locked up though? Too easy to protect the king. Maybe that's the point though... you end up in a kind of stable position and that's it?
- GHOST - All pieces are ghost pieces and can occupy the same square and thus cannot capture each other. All pieces can move anywhere on the board. I suppose you kind of need to display two chess boards/games simultaneously, but you'd run into the one king issue? Or not? Alternately it could be ghost the movie where an otherworldly force makes the move for you/guides your hand. Maybe another cursor/hand comes in and slowly tries to make a different move from yours? While Unchained Melody plays... maybe if you think for too long the music kicks in and it begins making a move for you :)
- DRESSAGE - Something about knight pieces and memorized sequences, could almost be like a Simon says thing
- KINGLIFE - Somehow have a camera in the king's head and just watch the game taking place via AIs?
- TRAGEDY - What would this be? Shakespeare?
- CONWAY - It's still a cool idea, maybe I could still make it do something
- MEMENTO - Playing a game backwards somehow? Could be that on any given move you can either move a piece "back" to where it came from, or you can place a new piece on the board and move some other piece to reverse a capture? And it's a race to reach the starting position???
- CHESSSS - Chess with snake rules somehow????? What would that be like? Pieces pull all pieces "behind" them in the same direction? Doesn't actually sound so snake-y though that basic idea is intriguing more generally
- COVID - Maybe it's about preventing the king from getting COVID, but pieces can become randomly infected at some point, and you try to give covid to the other team? Sounds over elaborate. The social distancing idea is nice too, but the starting position joke is already done.
- METAPHOR - Replace pieces with words or something and have the game appear to be some kind of story based on the interactions of those words (via chess moves)
- FLIPPER - Pieces flip over rather than slide? What would the implications of that be though? Sounds kind of dumb.
- FROGGER - Somehow, some way, a chess that's like frogger where your pieces have to wait for the alignment of moving squares to move around on the board... suspect it might just suck though
- MESS - Somehow the board is a mess? Pieces rotated awkwardly? Piled up? Can you even play? Do you have to tidy up instead, get all the pieces back to their proper locations? Single player?
- BLESS - Something about bishops and religion

## The short list

And then of all these, I think the ones that I could make a start on implementing and thinking might be of interest are:

- COMEDY (will need some laughtrack files though? Seems like the kind of thing that should be floating around online? But perhaps not? I guess I could just make it me laughing etc., that could be funny too)
- ESP (I mean, this is just a chess set obviously, maybe there could explicitly be some code underneath that is about being called through ESP? Could make a piece tremble sometimes to indicate that something might be working? Or even randomly move a piece sometimes? Just suggesting their ESP is not quite working?)
- 4'33" (probably this is too similar to ESP for both? Maybe not... and maybe there's something funny about exactly the same game being put forward as two different things?)
- HALVES (I really quite like this one. Deeply confusing. Can two different pieces of the same color occupy the same square???)
- IMMORTAL (this is a good one, though does require knowing about the game itself? But that's okay? Can be in the info panel anyway.)
- PACIFIST (no captures and that's all, I worried it would be uninteresting, but it's conceptually a thing)
- GHOST (after thinking about it, I really like the comedy value of referencing the movie, and for those many who don't know it it'll just be a ghostly presence trying to make your moves for you...)
- DRESSAGE (I think this can work as a sort of Simon says game for both sides? Maybe you win in a kind of sudden death thing?)

Maybes

- MEMORY (I think there's something super cool in here around blind chess and match games and stuff?)
- MEMENTO (I like the concept behind reverse-playing a game a great deal, but I have no idea how you would balance it at all? It's a neat idea though.)

So that is nine actual candidates. There really only one here that would be a proper game of chess (HALVES), and the rest are more comic interpretations of playing chess. I suppose DRESSAGE could be considered basically like a game.

A bunch of these can be made quite swiftly with only a couple seeming confusing (DRESSAGE, MEMORY and MEMENTO all seem a bit challenging).

---

# 3.5 games made (Tuesday, 14 April 2020, 15:33PM)

Today I've managed to put together 4'33", IMMORTAL, PACIFIST, and the start of ESP. They're all exceeding simple "variations" so it's not surprising they didn't take very long, but a couple of them are pretty satisfying.

4'33" came together kind of beautifully with the realization I could use the actual game title (and menu item) as a counter that tells you how long the performance has to go. It quits back to the menu when it's completed. (Could add applause at the end actually?) It's austere and quite nice I think, I actually like the core idea of being asked to sit and, I guess, think about chess rather than play it?

IMMORTAL works perfectly well, though it's obviously kind of frustrating. Showed it to Rilla who liked it more than I expected somehow. Needs an info panel at the very least to point people toward the correct move sequence. I've also wondered about literally indicating what the correct next move for black is, so you can just play through, but it's true that removes at least some of the mystery of the thing?

PACIFIST just works (even used `.filter()` because I'm so impressive with JavaScript arrays right?). I like that you can still get check and checkmate. It may invite a kind of playful movement of piece knowing you don't actually have to worry about being captured? Maybe you can move away from the whole war?

ESP is begun, but I've got a bit of a crisis in terms of how I'm positioning it. I started work on it thinking I'd have a whole kind of "fake ESP response" from the game, so pieces would jiggle around as if reacting to the player and maybe eventually a move would even be played. But the more I think about this the more silly it seems? Or rather, it seems dishonest because it's not really asking for ESP, it's just playing around with the idea of bad ESP? And it's not clear to me these variations have ever meant to be about that level of trickery? Sort of storytelling versus something more "pure" I suppose? Not sure where to land on that one yet.

---

# Is ESP real? (Wednesday, 15 April 2020, 9:56AM)

So do I make the ESP variant pretend that ESP is working, or do I make it actually depend on ESP? I kind of think it has to be the latter even if the former is way more funny to actually experience. There's something about it that bothers me, as it's no longer a _variant_ of chess, but rather a storytelling/narrative experience on the top of chess. Whereas, like MANIFEST, you can make a computer chess game that could be trained by... wait a second, ESP isn't right really is it, it's about _perception_ no influence. Fuck. Telekinesis then? Psionic? Yeah maybe.

Same principle applies despite the word obviously. Think I've really answered my question then.

---

# Where are we? Where are we going? (Wednesday, 22 April 2020, 14:51PM)

## Where are we?

A week later and where are we? We have

- 4'33"
- Dressage
- Immortal
- Pacifist
- Psionic

So I guess the proper new one is Dressage, which has been the most complex to implement, but which is a simple idea. Just the "Simon" game as applied with knight moves. Makes sense, work. Need to decide whether it goes on forever or if you can just have a tie? Maybe there are... 16 as the total pattern and it's a draw if you both reach that? Or maybe 8? Something like that makes sense.

## Where are we going?

The big question is what the final three games in the set should be.

### Halves

I've had a lot of trouble with this one the more I think about it. Questions like:
- Can a half-piece give check? Can it be part of a checkmate?
- Can two half-pieces of different types occupy the same square? (If so, how do you then choose which one you want to move? Seems kind of UI nightmare?)
- Can a whole piece move through a half piece or do they obstruct all pieces (except knights) in the same way as any other piece? E.g. if you develop e4 by half, can you then move your bishop? And if not, then the early game seems like it'll be a lot of double pawn moves to provide outlets? Or maybe a half piece can move through another half piece? That seems pretty damn stupid though.

Basically it seems philosophically shitty?

But that's really disappointing because I really like this idea in principle, damnit.

What happens if we do:

- Half pieces can give check (why not)
- Two half-pieces can only occupy one square if they add into a whole piece
- A half-pieces cannot move through each other

And we just try it and see if it makes any sense and/or is too boring for words?

### Ghost

I think this one is fine as an idea, no real need to think about it just need to implement the idea of an animated cursor coming onto the screen, choosing a piece and then a destination, unless you choose something yourselve in which case it moves away?

### Comedy

I basically still need to do more research to find laughs and think about the question of how they can sound "natural" in the context of the game. Basically it's very easy to write the world's simplest prototype (random laugh SFX after a given move) and see what it's like. It may even be that it doesn't need to sound like a consistent audience.

### Memory

Not really on the list, but I would like to think more about it? The principle is meant to be that you get shown the board (maybe once? maybe before each turn?) and then all the squares flip and you have to make your move based on memory. You'd choose the first square, it flips, and then you choose the destination, it flips, the move happens, and then they all flip back.

Maybe it's funnier and funner if you have to play memory chess all the way through? Seems worth trying out.

---

# Final stretch? (Friday, 24 April 2020, 20:06PM and Saturday, 25 April 2020, 19:59PM)

Well I think most the game is actually kind of together now?

Kicked off exactly two weeks ago today, so that's nice. Not that it's a race, but it's good to run fast when you can, right?

I think that in the end I have kind of two games that are perhaps actual games (MEMORY and DRESSAGE), another one that's at least edutainment (IMMORTAL), and then a bunch of quirks/jokes, which I think is a perfectly reasonable balance. Especially happy with how COMEDY turned out after worrying about creating a believable "studio audience" atmosphere throughout play. Thanks to the particular laughs I found, it turns out it's way better to have one person laughing, because it's so much more pointed.

Remaining is some tidying up of Dressage and a bit of stress testing I suppose?

If I were to (at some point) manage to make eight more chesses I would actually have managed to equal PONGS and BREAKSOUT which I find kind of remarkable. I didn't think I'd have been able to make quite so many as I've made! Nice one.

... the next day. Ummm, yes. Well it's going well then eh. I should just fix up the dressage stuff and release? I'll send it to Jim and Mary I suppose as well to stress test it on that front now? Yeah.
