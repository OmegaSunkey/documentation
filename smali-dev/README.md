# SMALI Patches

Newer Discord API behavior is harder to port or mimic with only Xposed-style hooks. To properly backport new Discord behavior, Aliucord now supports smali patches.

Please go to [Aliucord/Aliucord/main/patches](https://github.com/Aliucord/Aliucord/tree/main/patches) to know how to build smali patches.

To test these patches on your old device, you need an [old build](https://discord.com/channels/811255666990907402/811261478875299840/1428792362603380887) of Aliucord Manager, then use `patches:deployWithAdb`

## But how do I know what to port ?!?!?!?!?!?

You can use [Discord UserDoccers](https://docs.discord.food) to check most of the Discord API and Objects. Also check [how to find discord stuff](6_finding_discord_stuff.md)
