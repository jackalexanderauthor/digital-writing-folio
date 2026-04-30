### progress audit 15/04
> ***What is your early concept? Do you have any sketching/mapping done that details interactivity architecture? If so link to miro or other platform, or provide images of analogue working. What are the relations and storyworlds intenral and externally? What is left to chance and ergotics? Have you considered the visual aspect of your piece and what kind of images and design elements you will use?***

my first idea is one that i've had for a while about a game-type branching story depicting a series of conversations held on the night before a big event -- in my original imaginings this was like a big fantasy battle; the intention was that this is a rare chance for a small group of people to gather and reflect on their lives before they change forever. the actual scenario has changed a few times (last party before graduation, last dinner before moving cities, etc.), and i'm still not sure where i'll end up landing, but the structure as i imagine it is always the same: you play as one of a group of four, and you have the choice of three companions to talk to. you can have a conversation with each in turn, with the actual flow of the conversation greatly impacted by player choice. then, after all the conversations have concluded, the night ends and the scene of the following day plays out, itself being greatly impacted by the events of the conversation the night before.

it's a simple concept but i'm imagining a lot of interactivity based on the order of conversations you have, what happens in those conversations, and possibly some minor character creation elements? each of your companions would obviously have very different personalities and you'd have very different histories with each one that would change your dynamic. i've linked some drafts of the whole flow in my github, but i'll have to go through and create individual maps for each conversation individually, including optional branches depending on backstory/previous choices.

i haven't really considered including chance in the game -- it's not something i'm likely to put in considering how much i want to focus on player choice and character depth. maybe as a minigame within a conversation? flip a coin to see who has to do a truth or dare first e.g. 

### planning for week 6
so for assessment 2 i need to:

- give a 6-7 minute presentation in class
> - include a interactivity architecture sketch
> - show an early prototype of the work with min. 4 screens
> - reflect on development so far
> - speak to idea testing and iterations, including problems encountered and solving attempts

- have my in-class documentation on my github
> - submit my interactivity architecture maps

by week 7 i want to have:
1. clearly defined a setting, time period, and the basic identities of my three characters
2. have a more detailed architecture of one of the conversations, including at least three 'endings' and one minigame
3. have a first outline of the final scroll, including highlighted areas that can/will be changed according to player choices in the conversation

### week 7
did i achieve all that i set out to do? no. i locked down my setting and characters and started to script one of the first conversations, as well as layed out plans for the other two. i've come up with some initial "endings" each conversation can have as well as some interaction points, although they're not narratively important. More just reactive easter eggs. i haven't begun to think about the actual form of the final scroll just yet, but i have an idea for the deterministic structure. 

i developed a basic stat/trait system for the character, based along 3 axes: socialness, attitudes towards school, and self-confidence. different characters will respond differently to different personality traits, which will in turn affect their attitude towards the player character. when selecting passages for the final scroll, i'll take into account two variables: the relationship level each character has with the player, and the actual narrative decisions the player made. for example, a player who encourages character 1 to pursue their passion of photography while having a good relationship with them will still get a different outcome to a player who makes the same encouragements while having a bad relationship. To keep within scope, each character will have no more than 3 endings.

a lot of my work this week has been realising how much backend stuff i need to figure out before i can go about actually writing the work. i've realised a lot of my workflow has been backwards.

> iteration discussion

i've been fucking around a lot with different mechanisms behind the scenes. before i landed on the action/emotion system i'm working with now, i tried a lot of other ideas. i tried making a bunch of different variables that change different things but it ended up being wayyyyy too much to keep track of so i abandoned that idea. i also tried a more traditional rpg stat system using point allocation during character creation -- like you could assign scores to your charisma/insight/wisdom etc. i abandoned that bc it ended up being hard to integrate into the actual narrative world of the game. seeing a fallout style "you have a 20% chance of failing this check" kind of took out of the immersion of the world, and i didn't want to have to deal with random number generation or dice checks or whatever. i settled on my current solution as a sort of happy medium between the other options, taking what i liked from each. 

### week 8
as i've been locking in a lot more on the actual writing of the prose that makes up my piece, i've been running into one problem a lot, which is that a lot of the time there's overlap between my 6 stats (social/loner, confident/anxious, pro-school/anti-school). anxious and anti-school come up a lot together, but so do anti-school and loner -- but for different reasons. it's seriously slowing me down having to navigate the subtleties of each attitude 6 times over with every player choice, and i know that time lose is only going to compound and things get more complex.
the simple solution is, i think, to get rid of some of the stats, and change how they're used. the pro- and anti-school attitudes are the most obvious to cut, because i also think they're the weakest in concept. whether someone likes or doesn't like school is usually a symptom of their experiences rather than an independent emotion, y'know? cutting those two leaves me in an awkward spot, though, because i have three characters and four core stats. My original framework worked along the line of "each character corresponds to these stats", and if i want to continue that idea (which i do), i need three stats.
so which to cut? my remaining stats are:
- social
- loner
- anxious
- confident

which is, looking at them, only kind of two stats. social/confident and anxious/loner were other examples of stats with significant writing overlap i was struggling with, so i don't think it makes sense to cut one of the four and leave it outweighed by the others. i could bring back 'school attitude' as a third stat and have it work more like a scale rather than a score, but that seems like cutting off a broken leg. i'm just replacing one problem (too much writing) with another (having to keep track of another stat system) and not actually fixing anything. 
i originally positioned my stats along three axes, so i could just use those three axes as stats, going from 1-10 and starting each at 5, for example, but then i would have to be writing if/else statements that were checking for LOW scores as well as high ones, and again, it just doesn't feel as elegant. What i will do is bring back the school attitude stat and reframe it as an actual personality trait. So it'll go:
- social/confident -> social? popular? cool?
- anxious/loner -> anxious? depressed? introvert?
- pro-school -> nerdy? teacher's pet?

i don't want to set up an introvert/extrovert thing, and i don't necessarily want to tie "social" to "popular" so i think social, anxious, and nerdy are my stats. Delilah is social/anxious, casper is social/nerdy, and ferg is anxious/nerdy. Therefore, ferg dislikes social, delilah dislikes nerdy, and casper dislikes anxious
