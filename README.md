# Gatekeeper
Gatekeeper provides simple and local hosting to start your own Discord verification bot. This bot can allow you to weed out bots that spam incessantly so that you can enjoy your server. Please note that this repository is a more maintained and secure version of [Discaptcha](https://github.com/ahoys/discaptcha).

## Installation
1. Install [Node.js](https://nodejs.org/en/) for your CLI so that you can actually run the bot.
2. Create a new application and bot on your [Discord Developer Portal](https://discordapp.com/developers/applications) account.
3. Download the [latest release of Gatekeeper](https://github.com/wackyjackson/gatekeeper/archive/master.zip) and extract it if necessary.
4. `cd` to the general location of Gatekeeper; this should look something like `cd ./Desktop/Gatekeeper`.
5. Run `npm install`. If you encounter permissions errors, run `sudo npm install`.
6. Next, you'll need to configure the bot. You must do this before continuing. 

## Configuration
Any configuration made to Gatekeeper is done within `Gatekeeper/configs`

#### `/configs/auth.json`
This file stores information about your bot and client ID that you would get after making a bot and application on the [Discord Developer Portal](https://discordapp.com/developers/applications). If this file does not exist, create it under the `/configs` directory. It must have a `.json` file extension! If you are creating a new file, add the following code to it. If not, edit it accordingly.

```JavaScript
{
  "token": "KSJFUDIAODI2NTM1MjkyOTM4.DxsMDexampleA0M7Epfyh7KP43kMdKLD92",
  "id": "123456789012345678",
  "owner": "876543210987654321"
}
```
* `token:` replace the value following this with the token of your bot that is on the [Discord Developer Portal](https://discordapp.com/developers/applications). 
* `id:` replace the value following this with the Client ID of your bot. This is found under the General Information tab of your application on the [Developer Portal](https://discordapp.com/developers/applications). 
* `owner:` replace the value following this with your own Account ID. This can be done by simply right-clicking on your username and pressing Copy ID. 

#### `/configs/config.json`
This configuration file sets up and stores information about where the bot can operate and the behavior of it once deployed. The information in this bot is custom to you and needs to be edited accordingly.

```JavaScript
{
  "clientOptions": {},
  "timeToVerifyInMs": 60000,
  "guilds": {
    "277194040401854464": {
      "description": "MyExampleServer",
      "verificationRoleId": "533366845496098830",
      "moderatorRoleId": "533683841777401856"
    },
    "GUILD_ID_HERE": {
      "description": "GUILD_NAME_HERE",
      "verificationRoleId": "VERIFICATION_ROLE_ID_HERE",
      "moderatorRoleId": "MODERATOR_ROLE_ID_HERE (optional)"
    }
  }
}
```

*  `clientOptions:` this allows you to set up more advanced options for the initial connection with Discord. There is no need to add or remove this line as it can run safely without any content.
* `timeToVerifyInMs:` the value following this is the time in milliseconds that the user will have to verify before being removed from the server. 
* `GUILD_ID_HERE:` this text must be replaced with the ID of the server you wish to run this bot in. This can be done by right-clicking on the server's icon and pressing Copy ID. 
* `verificationRoleId:` change the value following this to the role ID of the role you wish to give to authenticated users. This can be done by doing the following: `Your Server > Settings > Roles` then right-click on the appropriate role and press Copy ID. 
* `moderationRoleId:` change the value following this to the role ID of the role you wish to give to moderators who can access more advanced commands within the bot. This is not necessary for the functionality of the bot.
