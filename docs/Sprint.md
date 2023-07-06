# Sprint Command in detail

`/sprint <duration> <when> <preset> <other>`

You can include one `<duration>`, one `<when>`, one `<preset>`, and any number of `<other>` parameters. They can be in any order. Everything is optional.

## Duration (how long?)

| Parameter | Example | How long will the sprint be? |
| --- | --- |--- |
| `<minutes>` | `/sprint 20` | 20 minutes |
| `for <minutes>` | `/sprint for 20` | 20 minutes |
| `until :<MM>` | `/sprint until :45` | From the start time until quarter-to (in almost all timezones) |

## Duration – random options

Undecided? You can choose a random length for your sprints.

| Wheel (long name) | Short Example | min – max | How long will the sprint be? |
| --- | --- | --- | --- |
| `micro` | `/sprint micro` | 1 – 6m |  μ-sprint for between 1 to 6 minutes |
| `flash` | `/sprint flash` | 2.5 – 10.5m |  Sprint for 2.5 to 10.5 minutes | 
| `not long` | `/sprint nl` | 5 – 12m |  Start a sprint for between 5 and 12 minutes |
| `not too long` | `/sprint ntl` | 5 – 20m |  Start a sprint that's randomly between 5 and 20 minutes |
| `however long` | `/sprint hel` | 5 – 40m | The original random sprint. Spin the wheel and start a sprint usually between 10 and 25 minutes, with a tiny chance of being around 5 or 40 minutes |
| `i don't know how long` | `/sprint idk` | 1 – 60m |  Sprint between 1 and 60 minutes, but with a 60× higher chance of a 1 minute sprint than a 60 minute sprint. How it's calculated: There's 60/1830 (=3%) chance of a 1-minute sprint; 59/1830 chance of a two-minute sprint, 58/1830 chance of a three-minute sprint, etc. |
| `not too short` | `/sprint nts` | 20 – 60m |  Sprint for between 20 and 60 minutes. |

## When?

| Parameter | Example | When will the example sprint start |
| --- | --- | --- |
| `<minutes> <minutes>` | `/sprint 20 5` | In 5 minutes, for 20 minutes. |
| `in <minutes>` | `/sprint in 5` | In 5 minutes |
| `at :<MM>` | `/sprint at :30` |  At half past the hour (for almost all timezones). You can leave off either the `:` or the word `at` (but not both). |
| `now` | `/sprint now` | Start immediately |
| `next <minute>` | `/sprint next 5` | Start once the big hand of your wall clock is pointing directly at a number (a multiple of 5 minutes) |
| `in <minutes> to <minutes>` | `/sprint in 5 to 10` | Starts the sprint in 5 to 10 minutes. If run this sprint command at 7:14, the sprint will start at 7:20 (in 6 minutes). Sprinto finds the best ("roundest") time to start your sprint in the period given. |
<!--TODO: next <minutes> grace <minutes> -->

Shortcuts: (finds a nice "round" time to start between these times)

| Shortcut | When will the sprint start |
| --- | --- |
| `now` | in 0s |
| `real soon` or `in a few ticks` | in 30s to 60s |
| `shortly` | in 1 to 2 minutes | 
| `soon` | in 2 to 3 minutes | 
| `iaf` or `in a few` | in 3 to 5 mins |
| `iab` or `in a bit` | in 2½ to 7½ mins |
| `aab` or `after a bit` | in 7½ to 12½ mins |
| `later` | in 12½ to 17½ mins |

## Presets

Convenient ways to start a sprint. 

| Preset | Meaning |
| --- | --- |
| (default) | `/sprint for 15m in 1m` |
| `quick` | `/sprint for 5m in 30s endtime 90s` |
| `long` | `/sprint 30 in 2.5 to 7.5 mins` |
| `marathon` | `/sprint for 60 in 7.5 to 12.5 mins endtime 10`|
<!-- | `dreamily` | `/sprint for 10 in a bit` (in 3 to 8 mins) | -->
<!-- | `just` | `/sprint now` | -->

You can override any part of a preset. For example, `/sprint quick 10` will `/sprint for 10 minutes in 30 seconds endtime 90s`

Please send feedback if you have suggestions for other presets or shortcuts.

## Other
| Keyword | Meaning |
| --- | --- |
| `quiet` or `quietly` | Don't ping anyone to announce the sprint. |
| `endtime <minutes>` or `fin <minutes>` | How long sprinters have to give their final word count. If you don't set this, the default ranges from 2 to 7.5 minutes depending on the length of your sprint. (calculated as: 1:30 min + 30s per 5 minutes of sprint) Use `/status` to check the endtime length for a running sprint. |
| `noff` | "no fast finish" — Always wait the full ending time for final word counts before showing the final results (instead of speeding it up if everyone's given their word counts). |
| `please` | ask Sprinto to do things he wouldn't normally, such as running a sprint up to 2 hours. |
| `lock` | Lock the sprint, meaning only a SprintMC can cancel it. (see: [[SprintAdmin]]) |
<!-- | `delay <minutes>` | (removed) Delay the opening of the sprint by this many minutes. I've effectively removed this feature as it didn't seem useful. I can enable it on your server if you really want but you'll have to let me know why you want it). If your start time is too far into the future, part of the time will be converted into a delay. | -->
<!-- | `help` | Gives you a link to this wiki page | -->

## `<minutes>`

Anywhere you see `<minutes>` you can also use seconds, e.g. `/sprint for 1000 seconds` or whatever you like really, e.g. `/sprint for .01 day` or `/sprint in 10m30s`. Sprinto uses [TimeSpanParser](https://github.com/quole/TimeSpanParser), which was developed for Sprinto.

## `:<MM>`

Where you see `:<MM>` it refers to a clock time without the hours. For example, to start a sprint at 7:35pm, you'd use `/sprint at :35`. There's no ambiguity because Sprinto can only start sprints less than an hour in advance. 

Use `/sprint now` to start a sprint immediately. If you try to start a sprint `at :35` when it's currently 7:35, Sprinto will think you want to start in about an hour (because 7:35:00 has already passed, so 8:35:00 is the next match for `:35`).

Note you can leave off the colon (`:`) so long as you remember to include the keyword `at` or `until`.

### Timezone notes

Sprinto doesn't know your timezone, and assumes you have a more typical one:

> Newfoundland, India, Iran, Afghanistan, Burma, Sri Lanka, the Marquesas, as well as parts of Australia use half-hour deviations from standard time, and some nations, such as Nepal, and some provinces, such as the Chatham Islands of New Zealand, use quarter-hour deviations. 
> — via Wikipedia, "[Time zone](https://en.wikipedia.org/wiki/Time_zone)"

Sorry, Sprinto can't adjust for Adelaidians and other half-hour or quarter-hour deviants, so if you are a timezone deviant please just pretend you're anywhere else in the world when using the `at :<MM>` and `until :<MM>` parameters. If this is an actual major issue for your Discord server, please let me know.
