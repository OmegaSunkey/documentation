# AliucordRN Plugin Documentation 

This documentation will only cover some basics. Anything outside of this documentation should be on the dev channel. You can also search on other plugins' source code. You can use the [plugin template](https://github.com/Aliucord/plugin-template-rn) so you can start making plugins for this project. 

# Information 
Plugins are made in JavaScript now. That means everything has changed, from patching to logic. If you want to develop plugins, you have to know basic JavaScript and React with React Native. 

Plugins have 2 lifecycle methods, start() and stop(). Pretty self-explanatory.

# Finding modules
We have the `aliucord.metro` module for searching and getting different modules. In fact, we have:

```js
aliucord.metro.getByProps("name")
aliucord.metro.searchByKeyword("name")
aliucord.metro.getById(Integer)
aliucord.metro.getByName("name")
```

We also have a [debug-ws-server](https://github.com/Aliucord/debug-ws-server) , a command-line program available on any platform (even android), which is useful for debugging (incredible). Every method above can be used in the command line, and it will give you the properties of the module. 
[!image](metroexample.jpg)

# Patching
We have some patching options. after() and before(), which are self-explanatory. (this needs better documentation)

# Commands
We also have / command support. You can register commands with 
```js
this.commands.registerCommand(
{
  name:..., 
  description:..., 
  options:[{...}], 
  execute:(args, ctx) => 
  {
    //command execution
  }
  
}
)
```
## Command Options
We have all the command options, `ApplicationCommandOptionType.`INTEGER; STRING; BOOLEAN; and others. You specify it in the options part, with `type: ApplicationCommandOptionType.STRING`. 
In `options`, it should look like this:
```js
options:[
  {
    name: "name", //Name of the option
    description: "description", //A good description of what the option does. 
    type: ApplicationCommandOptionType.STRING, //This is where you specify what the options should be. 
    required: true //can be false
  }
]
```
### Message from commands
You can make Clyde send a message when your command is executed. Just do `const Clyde = getByProps("sendBotMessage")` and in the execution block do `Clyde.sendBotMessage(ctx.channel.id, string)` with string being your message. 

You can also make the current user send a message. Do `import { MessageActions } from aliucord/metro` and in the execution block `MessageActions.sendMessage(ctx.channel.id, {content: string})`

# Settings
(settings section soon)

# Mobile development 
If you want to develop plugins without PC, then you need Termux and some code editor suitable for JavaScript. You can use the debug-ws-server in Android too, just remove the spawn command. You cannot (as of the time this was written) build plugins in your phone, so you can (ab)use GitHub Actions. 