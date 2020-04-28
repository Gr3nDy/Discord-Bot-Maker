# ![app icon](https://github.com/Gr3nDy/DBM-RawData/blob/master/Package/tokenme/Screenshot/icon.png) TokenMe | Wiki
# FAQ
Here's a list of Frequently asked questions regarding **TokenMe**;

# <h3>1. How do i fix "ERROR: The action does not exist!"</h3>
This means you're missing an action/mod please updgrade your DBM to Beta and install Mods,
You can find mods on DBM Network Server

# <h3>2. It gives me "Invalid Datatype" everytime i create a token</h3>
Make sure you put a correct configuration on datatype section [Here](./wiki.md#1-what-is-i-supposed-to-fill-on-datatype).
if you think you already put the configuration correctly and it's still doesn't work it might be your "Check Variable" Mod is outdated, since the command is using "Match Full regex" which you can only get on _betamods_. again please upgrade your DBM to Beta and install Mods

# <h3>3. Why do i have to fill my BOT Channel ID too</h3>
this is needed when a **Token** is `gifted` to a person, the token and bot channel will be sent to the person on DM.
However you can remove this function everytime [Here](./wiki.md#5-how-do-i-change-the-gift-token-messsage)

# <h3>4. How do i create a token</h3>
`[p]token create <datatype> <value> <duration>` <br> <br>
e.g `[p] token create coin 1500 7h` it'll create a token and will be expired in 7 hours<br>
**TokenMe** only Support Minutes/Hours/Days

# <h3>5. The bot logs keep spamming "Error with Event "Parse From Stored Json", Action #3: SyntaxError: Unexpected end of JSON input"</h3>
This is happen when the token didn't created correctly which causes the token.json empty,you can check if its empty by looking inside your bot folder `./resources/token` if there's no a folder called "token", you can create one inside the "resources" folder. You can fix this error by updating your Mods and switch to Beta or if its still happening you need to delete the "token" folder `./resources/token` and Re-Install [TokenMe Raw Data](help.md)

# <h3>6. The bot logs keep spamming "WebAPI Parser: Error: {"error":{},"statusCode":0,"success":false} stored to: [expires]"</h3>
Same as [FAQ #5](./wiki.md#5-the-bot-logs-keep-spamming-error-with-event-parse-from-stored-json-action-3-syntaxerror-unexpected-end-of-json-input) the token didn't created correctly which causes the bot can't read the token.json properly, this is might happen when you trying to edit the token.json manually or if you edited the "File Control Action" the wrong way. You can fix this error by updating your Mods and switch to Beta or if its still happening you need to delete the "token" folder `./resources/token` and Re-Install [TokenMe Raw Data](help.md)

# <h3>7. Error: ENOENT: no such file or directory, scandir './resources/tokenme/'</h3>
This error occured when the bot couldn't detect tokenme folder (most likely happens if you host your bot on glitch) there are 2 solution;<br>
1. Create a token by using the command (so it will automatically create tokenme folder) <br>
2. If the first one didn't work the you could manually add `tokenme` folder manually <br>
Add `tokenme` folder inside `'./resources/`


# Customization
Here's a few guides of how to customize your **TokenMe** command;
<br>(Some of these are optional)

# <h3>1. What is i supposed to fill on datatype</h3>
you supposed to fill a member data name by doing so it's allowing you to create the data into token <br>
<i>for an Example:</i> `/^(datatype1|datatype2|datatype3|datatype4)$/` to `/(coin|balance|XP|item|GEMS)$/` <br> <em>(REMINDER!!! CASE SENSITIVE)</em>
<br>
<br>
the format for `datatype` would be; `/^()$/`
<br>
use; `|`  to separate `datatype` from each other
<br>inserting invalid format might make the command not function

# <h3>2. How do i change the token length</h3>
Edit **Action #95 (Run Script)** & **Action #254 (Run Script)** <br>
`[...Array(9)]` to `[...Array(length)]`

# <h3>3. How do i change my token to look like a steam code</h3>
Replace **Action #95 (Run Script)** & **Action #254 (Run Script)** to <br>
```
const ran = [..."ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789"];
const com1 = [...Array(6)].map(i=>ran[Math.random()*ran.length|0]).join``;
const com2 = [...Array(6)].map(i=>ran[Math.random()*ran.length|0]).join``;
const com3 = [...Array(6)].map(i=>ran[Math.random()*ran.length|0]).join``;
var chars = com1+"-"+com2+"-"+com3
chars
```
# <h3>4. How do i change the `create` Token Messsage</h3>
`create` msg started from **Action #98 (Create Embed Message)**

# <h3>5. How do i change the `gift` Token Messsage</h3>
`gift` msg started from **Action #257 (Create Embed Message)**


[Back To TokenMe Page](https://github.com/Gr3nDy/Discord-Bot-Maker/blob/master/Raw-Data/tokenme/README.md)
