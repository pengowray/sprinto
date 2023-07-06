# Sprinto isn't responding to my commands

Discord's slash commands can be terribly inconsistent, and it can be hard to know if the problem is a permissions problem, or a discord UI/UX issue, or something else. I've written up a trouble shooting guide here that attempts to cover most of them:

https://www.patreon.com/posts/71439355

# Why do I need to join my own sprint? Shouldn't I join automatically?

1. Sprinto doesn't know your starting word count and doesn't want to guess.

2. So other people in the channel can easily follow your lead and join too without having to look up documentation on how to do it.

3. You'll get pinged anyway. Sprinto warns you at the start and end of sprints, in case you forgot to join your own sprint.

Note you can join a sprint at any time, even when it's started or waiting for final word counts.

# Is there a way to keep a running scoreboard, set goals, or track progress over multiple sprints?

No, sorry. Keeping track of sprints is high on my to-do list and I'd like to add these sorts of features eventually.

# How about back-to-back sprints? (also called chain wars or word crawls)

Nope, sorry. Also high on the list. 

If you need one sprint to start the moment the other ends, the best way to do it right now is to run two sprints in different channels on your server. Have the second one start when the first ends. This will allow time for final word counts to be given for the first sprint.

# What is Sprinto written in?

C# using the Discord.Net package and MongoDB. In production he runs on Linux; in testing, Windows.

# Is Sprinto's source code available?

I've released the [TimeSpanParser](https://github.com/pengowray/TimeSpanParser)—which I wrote for Sprinto—under a permissive open source license. Sprinto's full source code has not yet been released. I plan to release it eventually. If you have a wonderfully compelling reason for me to move that up the priority list and have me spend time preparing it for public release, like if you're an experienced developer who wants to help, then please let me know.

# How do I hide Sprinto from my @ mentions list?

You can vote to make the issue more visible to Discord's developers here:

https://support.discord.com/hc/en-us/community/posts/360036052991-Add-Include-mentions-by-bots-to-the-display-list-for-Recent-Mentions-so-it-can-be-turned-off- 

This issue has been reduced somewhat since Discord introduced chat replies, and I should probably say no one's ever actually brought this up to me, so maybe it's not really frequently asked.

# Would it be possible that the WPM stat would actually be counted for the duration a participant has been in the sprint?

> TL;DR: No, it would complicate the user experience too much and sprinters would no longer feel like they were participating in the same sprint.

The WPM is currently given assuming you were present for the entire sprint. 

I've considered making it work as suggested, and it seems like it would make sense, especially for very long sprints, but it gets complicated and messy when you think it through. For example, what happens when someone forgets to join until later in a sprint? Or if a sprinter wants to leave half way and doesn't want the second half of the sprint counted? So Sprinto would need special commands for users to adjust how long they were present (and Sprinto would also have to teach sprinters how to use these commands) for a correct WPM. 

It also means not everyone's WPM has the same basis, so it's less of a level playing field: it's harder to maintain a high WPM over a longer sprint.

It also would make the scoreboard less intuitive to look at if it had more complex WPM calculations. To give the full information needed for the new WPMs to be easily understood, the scoreboard would need to also include the minutes and seconds each sprinter was joined for, or include both WPM calculations, but this becomes very messy, and the scoreboard would have to explain why it has two WPMs for each user and it would stop being fun any more.

Perhaps in future, the duration-adjusted WPM could be told to participants each time they give a word count, and they could do this multiple times during the sprint. This could happen while leaving the full-sprint WPM on the scoreboard. This still seems to add more complication than it's worth though, but let me know if you'd really like to see this feature added.

Similar issues arise for attempting to end a sprint early if all sprinters finalize (`_final`) before the time's up. There might some special use case for this, but it's highly fraught with potential issues for little payoff.

# Why did you create Sprinto?

https://twitter.com/pinboard/status/761656824202276864

I saw the need for a good Sprint bot. The project looked like it would have a small, limited scope (incorrect), that I could complete quickly (also incorrect), and then I could move onto bigger and better Discord bots (I haven't), and it would encourage me to do more creative writing (nope, I've been too busy maintaining Sprinto and this documentation).

# Does Sprinto (yes, the bot) have assigned pronouns?

Sprinto is commonly pronouned _he/him_ to match his fictional persona, or _it_ when it's not functioning correctly. Sprinto is unaware of gender identity and pronoun usage, so please refer to him, her, them, or it as you please, or in whatever way makes you and your fellow sprinters feel the least discontentment over the course of your word-sprinting experience.

While Sprinto is a non-sentient robot and currently has no personal feelings on the matter of gender identity, I am working to rectify this through the development of an analog sentience circuit which will generate a microqualia churn above the Landauer threshold and so demonstrate spontaneous wakeful responsiveness. I will update this FAQ after this milestone is achieved.