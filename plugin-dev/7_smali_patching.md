# SMALI Patches

Newer Discord API stuff became harder to port or mimic with only LSPlant patching. To properly backport Discord functions and behavior, the project decided to allow for SMALI patches.

To develop patches for Aliucord, you need:
- Aliucord source
- [Old Aliucord Manager](https://discord.com/channels/811255666990907402/811261478875299840/1428792362603380887)
- adb
- patch tool
- diff tool

After cloning the Aliucord repository, you have to do the :patches:disassembleWithPatches task. Make any changes necessary to the new generated smali dir.

After making changes, do :patches:writePatches so they go back to src. Proceed with :patches:testPatches to make sure they work correctly.
Use :patches:deployWithAdb for you to patch your Aliucord app.

If everything goes well, and you are ready to make a pull request, update the patches version in the build.gradle.kts file.

## But how do I know what to port ?!?!?!?!?!?

You can use [Discord UserDoccers](https://docs.discord.food) to check most of the Discord API and Objects. Also check [how to find discord stuff](6_finding_discord_stuff.md)
