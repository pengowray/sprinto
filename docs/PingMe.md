## Pingme

After a sprint, participants will be tagged (@mentioned) at the start future sprints. 

If you miss three sprints or use `/forgetme` or `/sneak-away`, the pings will stop. 

Use `/pingme` to be mentioned when the next sprint starts even if you haven't sprinted recently (or to change your mind after `/forgetme` or `/pings-never`). You can also choose to never or always receive pings at the start of sprints with `/pings-never` and `/pings-always`

| Command | Description |
| --- | --- |
| `/forgetme` | Sprinto wont ping you at the start of sprints until after you join another one. |
| `/sneak-away` | `/leave` and `/forgetme` like a ninja: Leave the current sprint if you're joined and Sprinto wont ping you at the start of sprints until after you join another one. This command's response will only be seen by you. |
| `/pingme` | Sprinto will ping you at the start of the next 3 sprints in this channel. |
<!-- | `/pingme 10` | Choose how many sprints to be pinged at the start of. (e.g. 1 or 10 or 100). This will become your default after finishing a sprint. `_pingme 3` is what you typically start with. | -->
| `/pings-always` | Be included in the pings at the start of all future sprints in this channel, until you change the setting again. |
| `/pings-never` | Never ping you at the start of the sprints, even after you've done one. |
| `/pings-status` or `@sprinto pingstatus` | Check your ping status |

## Sprint MC only commands

| Command | Description |
| --- | --- |
| `/forgetuser 123456789` | Stops a user getting pinged at the start of sprints, as if they had typed `_forgetme` themselves. Replace `123456789` with the ID of the Discord user. If you can't see their user id, you might have to turn on "Developer Mode" in Discord settings, then "Copy ID" will appear when you right click the user. You can also use their user name (with no `@`), if they haven't left the server, but the ID is more reliable. |
| `@sprinto pinguser <user> <number>` | Turn pings on for a user, like if they typed `/pingme`. Replace `<number>` with the number of sprints. Default is 3. For "never" use 0. For always, use 1000. |
| `/setup-pingroles-set <role>` or `@sprinto always_ping_role <role>` | See: [SprintMC: Always ping a role at sprint start](SprintMC#always-ping-a-role-at-sprint-start) |

## Ping

| Command | Description |
| --- | --- |
| `@sprinto ping` | Check Sprinto's round-trip latency (nothing to do with sprint mentions) |

## Todo

* (TODO) guild or channel default number of pings
* (TODO) time-based, e.g. `/pingme for 15 hrs` or `/forgetme for 8 hrs` 