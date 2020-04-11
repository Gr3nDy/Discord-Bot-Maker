# ![app icon](https://github.com/Gr3nDy/Discord-Bot-Maker/blob/master/Raw-Data/tokenme/Screenshot/icon.png) TokenMe
[![release](https://img.shields.io/static/v1?label=release&message=1.1.2&color=red)](https://github.com/Gr3nDy/Discord-Bot-Maker/blob/master/Raw-Data/tokenme/README.md)
<br>
<b>Update:</b> Version 1.1.4 will be realeased soon. [Keep your eyes on!](https://raw.githubusercontent.com/Gr3nDy/Discord-Bot-Maker/master/Resources/WATCHING.gif)
<br>
<br>
Convert <b>Member Data</b> into a reedemable <b>Token</b> <br>
![gif](https://github.com/Gr3nDy/Discord-Bot-Maker/blob/master/Raw-Data/tokenme/Screenshot/GIF.gif)

<b>Usage</b>
* `[p]token create <datatype> <value> <duration>`
* `[p]token gift <user> <datatype> <value> <duration>`
* `[p]token list`
* `[p]token check <token>`
* `[p]token delete <token>`
* `[p]redeem <token>`

# Installation

<b>Commands</b>

* [TokenMe](https://raw.githubusercontent.com/Gr3nDy/Discord-Bot-Maker/master/Raw-Data/tokenme/Commands/tokenme.json)
* [Redeem](https://raw.githubusercontent.com/Gr3nDy/Discord-Bot-Maker/master/Raw-Data/tokenme/Commands/redeem.json)

<b>Events</b>

* [Loop 1](https://raw.githubusercontent.com/Gr3nDy/Discord-Bot-Maker/master/Raw-Data/tokenme/Events/Loop%201.json)
* [Loop 2](https://raw.githubusercontent.com/Gr3nDy/Discord-Bot-Maker/master/Raw-Data/tokenme/Events/Loop%202.json)

Copy <b>Commands</b> & <b>Events</b> and import to
DBM.
* 1.Create New Command
* 2.Right click the command
* 3.Select Edit Raw Data
* 4.Paste Raw Data
* 5.Click on save
* 6.[Configure](#Configuration) the Raw Data

# Configuration

<b><ins>Commands:</ins></b>

<b>Token</b>
* Put your <b>Log Channel ID</b> to <strong>Action #5 (Find Channel)</strong> 
* Put your <b>Bot Channel ID</b> to <strong>Action #7 (Find Channel)</strong> 
* Edit <strong>Action #9 (Run Script)</strong>  and add any member data you'd like to be able to create token <br>
  <i>for an Example:</i> `/^(datatype1|datatype2|datatype3|datatype4)$/` to `/^(coin|balance|XP|item|GEMS)$/` <br> <em>(REMINDER!!! CASE SENSITIVE)</em>

<b>Redeem</b>
* Put your <b>Log Channel ID</b> to <strong>Action #5 (Find Channel)</strong> 
<br>


<b><ins>Events:</ins></b>

<b>Loop 1</b>
* On <strong>Action #2 (Loop Through List)</strong> Set it to call Event <b>Loop 2</b>

<b>Loop 2</b>
* Put your <b>Log Channel ID</b> to <strong>Action #6 (Find Channel)</strong>

# Changelogs

<details><summary>1.0.0</summary>

* Added logs for `gift`
* Added logs for expired token
* Added `check`
* Bugs fixed
</details>

<details><summary>1.0.2</summary>

* Added logs for `create`
* Added logs for `redeem`
* Simplified embed design
* Bugs fixed
</details>

<details><summary>1.0.4</summary>

* Fixed Insensitive Tokens
* Moved "Bot Channel ID" for `tokenme`
* Bugs fixed
</details>

<details><summary>1.0.6</summary>

* Fixed `redeem` Embed
* Added `if gift failed` Message
</details>

<details><summary>1.0.8</summary>

* More Relaxed `Duration`
* Fixed Duration Logs
* Bugs Fixed
</details>

<details><summary>1.1.0</summary>

* Fixed Missing `Send Embed Message`
* Bugs Fixed
</details>

<details><summary>1.1.2</summary>

* `Redeem` also log the Data Type and Value now
* Fixed `Match Exactly` Token not function
</details>



# Note
⚠️<b>Make sure you've installed <em>betamods</em> on your DBM</b>⚠️
<br>
<br>
This Command is intended to be used only for one server
<br>
<br>
Keep in mind that member data are case sensitive, so put the correct member data on `datatype` configuration or else it'll create a new member data
<br>
<br>
[TokenMe | Wiki](https://github.com/Gr3nDy/Discord-Bot-Maker/blob/master/Raw-Data/tokenme/wiki.md)
