# Finding Discord Stuff

To make any plugin that modifies discord classes and methods, you need to find what method does what and in which class it is. There are two ways to do so:

If you are comfortable with decompiling the entire discord source code, you can use JADX with the following command:

```
jadx --export-gradle --show-bad-code --fs-case-sensitive --respect-bytecode-access-modifiers --no-inline-methods --no-inline-anonymous --no-inline-kotlin-lambda --output-dir decompiled base.apk
```

If you use Aliucord's [fork](https://github.com/Aliucord/jadx) of JADX you can add the `--no-generate-kotlin-metadata` flag to remove the `@Metadata` annotation on most classes.

Either way, you can check [RazerTexz's repo](https://github.com/RazerTexz/Discord-JADX) to see the Discord source code.

You can use the [Developer Assistant](https://play.google.com/store/apps/details?id=com.appsisle.developerassistant&hl=en_US) app for finding view names while running Aliucord.
