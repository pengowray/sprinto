# Miscellaneous commands

Less useful commands. You don't need any of these commands, but they're documented all the same.

| Command | Description |
| --- | --- |
| `@sprinto parse [time]` | Test Sprinto's time parser. e.g. `@sprinto parse 1 day 3,000,000 seconds` — see [TimeSpanParser](https://github.com/quole/TimeSpanParser) for more. |
| `@sprinto invite` | Create an invite link to take Sprinto to another server. Also gives a link to the support server. (Both links are in the footer of this wiki) |
| `@sprinto sprintmc` | Just tells you about the [[SprintMC]] role, and provides help to set it up. |
| `/admin-refresh-active-role` or `@sprinto refresh_active_role` | Moves people in and out of the `@Active Sprinter` role, in case some people are stuck in the wrong place. Can be used by anyone. For more info: [[ActiveSprinter]] |
| `@sprinto prefix` | Show Sprinto's prefix on your server, which is now always `/`. Unfortunately, this can no longer be changed. |

## Sprint-related

See [[Home]] for Sprinto's main commands.

| Command | Description |
| --- | --- |
| `/final` or `@sprinto final` or `/words final` | Finalize your word count, so Sprinto won't wait for you to update it later (or will stop waiting if the sprint is over).  |
| `/final` count: `1200` | Finalize your word count with 1200 total words. Same as `/words` count: `1200 final` |
| `@sprinto who` | Lists active sprinters in the channel. Sprinters who have voted to `_cancel` are marked with "❌" |
| `@sprinto starting 1000`| aka `@sprinto tare`. Change your starting word count without changing your current word count. I'm not sure why you'd want to do this. Typically instead of using this, you'd just `/join` again with a different starting word count, and then set your new word count with `/words`. |
| `@sprinto rejoin` | Rejoin a sprint you left with `/leave`, restoring your previous word count. |
| `@sprinto status` | Check your word count, time remaining and number of active sprinters. Will give your `/pings-status` if no sprint is running |
| `@sprinto close` or `@sprinto stop` or `@sprinto end` | These will tell you to use `/cancel` or `/leave` instead |
| `@sprinto wc_undo` / `@sprinto wc_redo` | undo or redo your last `/words`, `/join` or other command which changed your word count or sprint status. (This was the start of a general undo feature) |
<!-- | `/words reset`| Same as `/words 0 new` | -->