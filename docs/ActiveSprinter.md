The `@Active Sprinter` role is an extra thing admins can set up, but is not necessary for the running of Sprinto. It gives sprinters currently participating in a sprint (in any channel) the role `@Active Sprinter`. You can use this to make sprinters pop up to the top of the server's members list under the "Active Sprinters" role banner, which lets others on the server know a sprint is happening. Having the role can give sprinters a special color username while they're participating in a sprint, as well as a special badge next to their name (requires a Discord boosted servers). 

If the `@Active Sprinter` role is mentionable, it can also be used to mention (ping) active sprinters, however Sprinto itself does not use the role for this purpose. Sprinto doesn't use it because the same `@Active Sprinter` role is used for every sprint channel, so it might ping the wrong people if there are two sprints running at the same time in different channels. Instead, Sprinto tags the individual sprinters who have joined the sprint.

The `@Active Sprinter` role color, badge icon and position in the members list, and mentionability are all standard Discord features that an admin can set up in the server's role settings.

These commands are available to guild administrators and members with "Manage Roles" or "Manage Server" permissions:

| Command | Description |
| --- | --- |
| `@sprinto create_active_role` | Create a role named `@Active Sprinters` for Sprinto to use on your server. The role is created as _mentionable_, _hoisted_ under Sprinto's highest role, and with no permissions nor color. If can't be created, it will tell you why.
| `@sprinto repair_active_role` | Sets the `@Active Sprinters` role to be hoisted, mentionable and its position to be under Sprinto's highest role. |
| `@sprinto refresh_active_role` or `/admin-refresh-active-role` | Attempts to fix membership of the @ActiveSprinter role for special cases where people are stuck with or without the ActiveSprinter role that they should or shouldn't have. This command should never be needed, but it's here in case. Despite "admin" in the name, this command can be used by anyone. |

Admins can use `@sprinto create_active_role` to set up an `@Active Sprinter` role. Once it's created, anyone who joins a sprint will now get automatically added to the `@Active Sprinter` role during the sprint. At the end of the Sprint everyone is removed from the role. Works with multiple sprint rooms.

If you no longer wish to use this feature, just delete the `@Active Sprinter` role.

`@sprinto create_active_role` will give you help or advice if there's problems with the role's set up or Sprinto's permissions for using the role.

## Customizing

Under **Server Settings > Roles** you can customize the Active Sprinter role.

1. (optionally) Change the color — if you want sprinters to have a different color when sprinting, feel free to change the color of the role.

2. (optionally) Rename the role (a little) — Sprinto will still find the role if it's named slightly differently: You can remove the space, change the capitalization or add a plural ending or anything else to the end. For example, the following are all valid names for the role: `@ActiveSprinter`, `@ActiveSprinters`, `@Active Sprinter`, `@Active Sprinters`, `@active sprinters rock`. Let me know if you feel you need a different name. I haven't allowed it to be too customizable to avoid potential conflicts or security issues when combined with other bots.

3. (optionally) Change the position of "Active Sprinters" on the members list: Under **Server Settings > Roles**, drag Sprinto's role at the top (or as high as you're comfortable) and drag the Active Sprinter role just under it. This way everyone on your server will more easily see a sprint is running.

Notes: The command `@sprinto create_active_role` will already place the role as high as Sprinto is allowed. Bots cannot control roles that are higher than their own highest role, so if you want to move ActiveSprinter higher (to be more visible), drag one of Sprinto's roles to a higher position first and place ActiveSprinter just below that role. If Sprinto doesn't have any roles, then he probably doesn't have Manage Role permissions which he needs for this feature, so invite him to your server again (there's a link at the bottom of the page) or set up a role for him. Note you don't need to display Sprinto on the members list at the position of his highest role: you can turn off "heisting" from Sprinto's top role (uncheck "Display role members separately from online members"). After changing role positions around, you can use `@sprinto create_active_role` or `@sprinto refresh_active_role` to check everything is OK. This all sounds needlessly complicated and I feel there should be a better way to explain it all but there it is.

4. (optionally) Note you can create a role from scratch named "Active Sprinters" and it will still be used by Sprinto, but using `@sprinto create_active_role` is recommended because it tells you if there's an issue. (You also also use it after creating the role manually)

