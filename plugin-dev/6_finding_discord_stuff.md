# Finding Discord Stuff

To make any plugin that modifies discord classes and methods, you need to find what method does what and in which class it is. There are two ways to do so:

If you are comfortable with decompiling the entire discord source code, you can use JADX with the following command:

```
jadx --export-gradle --show-bad-code --fs-case-sensitive --respect-bytecode-access-modifiers --no-inline-methods --no-inline-anonymous --no-inline-kotlin-lambda --use-source-name-as-class-name-alias if-better --output-dir decompiled base.apk
```

If you use [Juby210's fork of JADX](https://github.com/Aliucord/jadx) you can add `--no-generate-kotlin-metadata` if you do not want big kotlin metadata walls.

Either way, you can check [RazerTexz's repo](https://github.com/RazerTexz/Discord-JADX) to see the Discord source code.

You can use the Developer Assistant app for finding view names while running Aliucord.
