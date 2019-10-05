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
