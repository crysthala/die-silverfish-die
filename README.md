# die-silverfish-die
Kills silverfish the moment they spawn. Hopefully, performance impact should be minimal.

## Installation
Press the "Clone or Download" button on this page and select "Download ZIP". Open the .zip archive and extract the "die-silverfish-die-master" folder to the saves/world-name/datapacks folder. If you're currently running Minecraft, you'll need to enter the /reload command before it'll start working. You can confirm it's loaded by using /datapack list.

### I have to do that for every save??
Yes. There are mods that can automatically load datapacks for you, but on vanilla, the only way to load them is to manually add the data pack to individual saves. No, I don't know why Mojang did this.

### How does this work?
The file "tick.json" located in minecraft\tags\functions\ holds an array of strings that point to functions, in the format "namespace:function_name". Every tick, vanilla MC will check the loaded datapacks for this file and run all the functions listed inside. "Functions" are simply text files that hold a list of commands. In this case, I simply put a /kill command that targets silverfish only into the tick.json file, and thus, every tick, Minecraft will smite any silverfish the server has loaded. Bye Felicia~~
