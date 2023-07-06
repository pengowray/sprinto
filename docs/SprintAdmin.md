Commands available to guild owners, administrators and people with a role named SprintAdmin. Some commands are also available to people with a SprintMC role. 

# Sprint Admin intro

A _Sprint Admin_ (A) is someone with extra privileges on a server. A server's owner, its administrators, and anyone with a role named `Sprint Admin`. For simplicity, they'll all be called _SprintAdmin_ here. Sprint Admins can configure Sprinto, for example, they can set which channels sprints run in, or remove all users from the ping list.

Sprinto considers anyone who has a role named `Sprint Admin` or `Sprint Admins` (space optional, any capitalization) to be a _Sprint Admin_.

# Sprint MC intro

A _Sprint MC_ (MC) is a less powerful role (which Sprint Admins also automatically have). Sprint MCs can cancel sprints, or remove a single user from the the ping list, or run "locked" sprints which ordinary users cannot cancel.

Sprinto considers anyone who has a role named `Sprint MC` or `Sprint MCs` (space optional, any capitalization, and will also accept Sprinto MC) to be a _Sprint MC_. Additionally anyone with Sprint Admin powers also has Sprint MC powers.

# Create the roles

Sprinto doesn't create the "Sprint MC" or "Sprint Admin" roles for you, so you'll have to create them the same way as creating any other Discord role. The roles are both optional. There's no requirement to have anyone with either role to run sprints. On a small server you might create the Sprint MC role and give it to everyone just so everyone can easily cancel sprints.

More fine grained control of Sprinto privileges is not available. If you need a more specific role for your server please provide `/feedback` and tell me about your situation.

## Notes about Sprint MC and Sprint Admin commands

* "Please" is required for many commands. Instead of "please" you can also use "pls", "thanks" or "merci". Please is also used for some non-admin commands like to set your word count to a negative number. 
* More SprintAdmin and SprintMC commands may be added in future.
* Guild owner and administrators automatically have Sprint Admin and Sprint MC powers.

# SprintAdmin (A) and SprintMC (MC) commands

## General

| Command | Description |
| --- | --- |
| `/admin-force-cancel` or `@sprinto cancel please` | (MC) Forces a running sprint to end, regardless of how many sprinters have joined. |
| `/sprint ... lock` | (MC) Begins a sprint which cannot be cancelled except by a Sprint MC. See [[Sprint]] for the other parameters you can add to a `/sprint` |
| `/sprint ... please` | (MC) SprintMCs who add "please" to a sprint command can set it to run for longer, or have slightly increased "ready" time before it starts. |
| `/admin-force-nudge` or `@sprinto nudge please` | (MC) Moves the sprint on to the next stage immediately, typically only used for testing or debugging purposes. |
| `/admin-forget-user 123456789` or `@sprinto forgetuser 123456789` | (MC) Stops a user 123456789 getting pinged at the start of sprints, as if they had typed `/forgetme` themselves. Replace `123456789` with the ID of the Discord user. If you can't see their user id, you might have to turn on "Developer Mode" in Discord settings, then "Copy ID" will appear when you right click the user. You can also use their user name (with no `@`), if they haven't left the server. Use `/admin-forget-all-users` or `@sprinto forget_all_users` (A) to forget all users. |
| `@sprinto pinguser <user> <number>` | (MC) Turn pings on for a user, like if they typed `/pingme`. Replace `<number>` with the number of sprints. Default is 3. For "never" use 0. For always, use 1000. |

## Sprinting channel whitelist (Sprinto Setup)

| Command | Description |
| --- | --- |
| `/setup-set-allowed-channel` or `@sprinto set_sprinting_channel_here` | (A) Whitelist a channel to allow sprints to be run in it. Multiple channels can be selected by typing this in multiple channels. |
| `/setup-unset-allowed-channel ` or `@sprinto unset_sprinting_channel_here`| (A) Remove a channel from the whitelist. If none are left on the whitelist, sprinting is not restricted to any channel. |
| `/setup-reset-sprinting-channels` or `@sprinto reset_sprinting_channels` | (A) Clear and stop using a whitelist. Allows sprints to be run in all channels (the default). |

Note: Sprinto does not have a concept of secret or hidden channels. Sprinto will attempt to point Discord users to a sprint room even if the user doesn't have permission to see or use that channel.

## Always ping a role at sprint start

If members of your Discord server can self assign roles (for example via another bot), then you may have a role named "@Sprinters" and want Sprinto to always mention (ping) those users when a new Sprint starts. You can do that with: `/setup-pingroles-set Sprinters` or `@sprinto always_ping_role Sprinters`

| Command | Description |
| --- | --- |
| `/setup-pingroles-set <role>` or `@sprinto always_ping_role <role>` | (A) The `<role>` will always be pinged whenever a new sprint starts. Replace `<role>` with the name or ID of a role. You may wish to use this in combination with `_setAutoPings off` (to stop Sprinto pinging individual users at the start of a sprint) |
| `/setup-pingroles-remove <role>` or `@sprinto never_ping_role <role>` | (A) Remove `<role>` from the "always ping" list. |
| `/setup-pingroles-clear` or `@sprinto clear_ping_roles` | (A) Remove all roles from the "always ping" list. |
| `/setup-pingroles-list` | List roles that will always be pinged |

Notes:
* These settings are per channel: if you want a role pinged in multiple sprint channels then use `/setup-pingroles-set <role>` in each. Multiple roles and different combinations of roles can be used in each channel.
* These commands are only for mentions (pings) at the start of sprints. These commands will not cause Sprinto to assign anyone to the roles.
* Sprinto will still track recent sprinters and ping them (as well as the roles you choose). If sprinters want to always be pinged they can also use `/pings-always` to be specifically pinged at the start of sprints.
* Add `noping` to a sprint command, e.g. `/sprint for 30 noping` to start a sprint without pinging any roles or user.

## Channel settings

All settings can be set to `on`, `off` or `default`

| Command | Description |
| --- | --- |
| `/settings` | Display values of channel settings. |
| /setup-set-show-patreon-requests or `@sprinto setShowPatreonRequests off` / `on` | (A) Show / don't show requests to join Sprinto's Patreon (or to buy Sprinto merch) at the end of sprints. You can also use `_patreon` and `_merch` for links. |
| `/setup-set-show-quotes` or `@sprinto setShowQuotes off` / `on` | (A) Hide or show quotes at the end of sprints. Quotes are meant to be thought provoking and inspiring. If you find ones that are instead overly prescriptive (about grammar or what a "real" writer is), or otherwise problematic, please report them by leaving `_feedback` with the quote, or mention it on the support Discord. |
| `/setup-set-show-ps` or `@sprinto setShowPS off` / `on` | (A) Show or hide all post-sprint text. Turning this off will hide quotes, updates, combined word counts, `_forgetme` help, and everything else which would otherwise be shown after the scoreboard. |
| `/setup-set-autoping` or `@sprinto setAutoPings off` / `on` | (A) Set whether sprinters who join should automatically be pinged (mentioned) at the start of the next few sprints. If off, users will not be added to the list of users be pinged at the start of future sprints. Users can still manually use `_pingme` or `_always`. Even with autopings off, the `_always_ping_role` setting will be respected, so, for example, if you have a @sprinter role which users can add themselves to and use `@sprinto always_ping_role @sprinter`, then Sprinto will alert them of new sprints via that role. Use `@sprinto forgetallusers` (A) to remove all existing individual user pings. |
| `/setup-set-show-walltime` or `@sprinto setShowWallTime off` / `on` / `sometimes` | (A) Show or hide display of the ending "wall time" when sprint starts. e.g. "(Runs until ⏰ :30)". With `sometimes` (the default) it will only be shown if the sprint ends near an exact minute. With `on` it will be always shown (at least for sprints longer than 2 minutes). Wall time also shown with the `_time` command for both `on` and `sometimes`. |

## See also
* [[Setup]] (setting up Sprinto)
* [[ActiveSprinter]] (another role used by Sprinto)
* [[Voice]] 
