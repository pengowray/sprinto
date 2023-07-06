# Setting up Sprinto (Server owners/managers)

**Steps:**
1. If you can see Sprinto already:

![image](https://user-images.githubusercontent.com/800133/186021910-5f43df64-c614-42f2-982a-d956ca28cc0d.png)

Or via the web:

1. **[Invite Sprinto](https://discord.com/oauth2/authorize?client_id=421646775749967872&scope=bot&permissions=2419424576)** — Bring Sprinto to your Discord server. 

![Screenshot](https://i.imgur.com/baDQffR.png)

2. That's it. You're ready to Sprint! Type `/sprint` in a channel to start a sprint.

## Troubleshooting and notes 

* All requested permissions are optional: If you're worried about a robot uprising, you can uncheck them all and still run sprints just fine. But they are recommended for extra features (current and future).

* Make sure you're logged in at [discord.com](https://discord.com/) and try to invite Sprinto again.

* If you don't have permission, pass on the invite link to the server owner or someone who has permission to add bots: https://discord.com/oauth2/authorize?client_id=421646775749967872&scope=bot&permissions=2419424576 or give the link to this page. <!-- or use Sprinto's `/setup invite` command... which sends you here now. -->

# Optional steps

**But what else can I do as a server admin?**

3. **Create a dedicated sprint room.** Sprinto usage can quickly overwhelm any chat room, so almost all servers create a dedicated sprint channel with a name like `#writing-sprints`, `#sprints-and-excerpts` or something thematically appropriate for their server like `#sprinting_dojo`. Sprinto often fails to see any usage when he has to share a general `#bots` channel. Some servers even have two sprint channels, one for short spontaneous sprints (perhaps 15 or 30 minutes) and one for longer, pre-planned sprints (up to an hour). Sprints started in different channels run independently. You cannot run more than one simultaneous sprint in one channel.

4. **Create a Sprint MC role.** If you create a role named "Sprint MC" (or "Sprint MCs", any case), anyone assigned the role will have additional powers to help run and manage sprints, such as forcing a sprint to end with `/cancel please`. The guild owner and administrators also have Sprint MC permissions automatically. _See **[[SprintMC]]** for more_

5. `/setup create_active_role` to set up an `@Active Sprinter` role. Active Sprinters get automatically added to the `@Active Sprinter` role during the sprint if it exists, so you can see sprinters (and that a sprint is happening) in the members list. _See **[[ActiveSprinter]]** for more_

6. What about **Sprinto's permissions**? Sprinto currently needs no more than the default permissions which @everyone else has also has by default: to "Read Messages" and "Send Messages". Sprinto will also need "Manage Roles" for the @Active Sprinter (above).

7. So then why did Sprinto ask for **more permissions** when I invited Sprinto? So far, these are mostly for future features (except Manage Roles). Until recently Sprinto asked for no permissions, so use the "invite" link at the top of the page to re-invite him to add these new permissions. Sprinto will need the following for current and planned features: manage roles (for active sprinter), send TTS messages (to allow announcements; future planned feature), priority speaker (to allow pings in a voice channel; in future), and manage messages (to clean up word count commands; in future). Regardless, he'll continue to work with only the default read & send messages permissions.

8. Sprints in the wrong rooms? If you want to prevent anyone starting a sprint outside of the sprint rooms, you can use `/setup set_sprinting_channel_here` in the channel or channels where you want sprints to be run. _More info: [[SprintMC#sprinting-channel-whitelist-sprinto-setup]]_ Alternatively, you can remove Sprinto's "Send Messages" permission in rooms you don't want Sprinto to respond in, or remove his "Read Messages" permission in channels you don't want Sprinto seen in.

9. To help users see Sprinto you can order his role to place him higher in the members list. Server Settings > Roles > Drag the _Sprinto_ role up as high as you're comfortable. (Note: He won't have a "Sprinto" role if he's only got minimum permissions)

10. If other bots have similar commands which may confuse or trip up sprinters, you can remove their permissions in your sprinting channels to make it easier to use and find Sprinto's commands. Similarly you can remove permission to use Sprinto commands elsewhere.

11. **Rename Sprinto** and give him a thematically suitable nickname on your server, such as Sir Sprinto Esquire. (Right-click on Sprinto and "Change Nickname")

12. Feel free to **plug your writing server** on #plug-your-writing-server on Sprinto's support server.
