# Sprinto Voice

Sprinto can join a voice channel during a sprint and make sounds at the start and when time's up. It's not consistently reliable and difficult to debug (I'm yet to work out a way to tell if it's been working or randomly stopped for someone or everyone). 

Because of possible reliability issues Sprinto Voice is in perpetual beta. These commands will not be available on your server unless you've requested it. Ask on the Sprinto Planet discord if you'd like to try it.

# How it works

Sprinto will automatically join the first voice channel it finds with "sprint" in the name (e.g. "🔊 Sprinting talk"). You can set it manually with `@sprinto set_voice_home_here`, or disable Sprinto using voice with `@sprinto voice_home_off`. If Sprinto's previous voice channel is removed you may have to use `@sprinto reset_voice_home` to have Sprinto find another one.

# Commands

The only setup required is creating a Discord voice channel with a name starting "sprint", for example: `🔊 Sprinto-chat`. However if you'd like to choose a different voice channel or turn voice off, you can use the commands below.

Note again, this feature isn't enabled unless your server has been added to a list of enabled servers. Request beta voice access on the Sprinto Planet discord.

| Command | Description |
| --- | --- |
| `@sprinto set_voice_home_here` | (A) Join a voice channel first, then enter `@sprinto set_voice_home_here`. This sets Sprinto's voice channel (server-wide setting) |
| `@sprinto reset_voice_home` | (A) Set Sprint's voice channel to the default (i.e. any voice channel with "sprint" in the name) |
| `@sprinto voice_home_on` | (MC) Allow Sprinto to join voice channels on your Discord server (defaults to on) | 
| `@sprinto voice_home_off` | (MC) Stop Sprinto joining voice channels |
