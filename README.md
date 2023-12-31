## Discord-Waitingroom-Bot

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Tomato6966/)
[![Ask Me Anything !](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg)](https://GitHub.com/Tomato6966/Ask-Me-Anything)
[![Support Server](https://img.shields.io/discord/591914197219016707.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/fS6qBSm)

A basic, easy to setup Waiting Room Bot to play an audiofile on your pc / a stream!

## [**DISCORD SUPPORT SERVER INVITE**](https://support.milrato.eu)

## Installation | How to use the Bot

 **1.** Install [node.js v12](https://nodejs.org/api/cli.html#cli_unhandled_rejections_mode) or higher

 **2.** Install [ffmpeg@latest](https://ffmpeg.org) 

 **3.** Download this repo and unzip it    |    or git clone it
 
 **4.** Install all of the packages with **`npm install`**     |  the packages are   **`npm install node.js discord.js @discordjs/opus`**
 
 **5.** start the bot with **`node index.js`**

## Usage - config.json

```javascript
{
  "token": "",        // Fill in your Bot token
  "voicechannel": "", // Voice Channel Id for your Bot Channel
  "guildid": ""       // Guild Id of your Server
}
```

## Usage - index.js  | function radioexecute()  | Line 26-34

```javascript
async function radioexecuteadmin() {
    const voiceChannel = client.guilds.cache.get(config.guildid).channels.cache.get(config.voicechannel); //define the Voice Channel
    await voiceChannel.leave(); // leave the channel
    await delay(300); // wait 300ms to provent a bug
    var connection = await voiceChannel.join();//join the channel and
    await connection.voice.setSelfDeaf(true); await connection.voice.setDeaf(true); //selfdeaf
    const dispatcher = connection.play('./audiofile.mp3'); //You can replace the './audifile.mp3' with any sort of Radio stream for example: 'https://streams.ilovemusic.de/iloveradio17.mp3'
    dispatcher.on("end", end => { radioexecuteadmin() });
}
```

## **NOTE:**

*Make sure that you have install [FFmpeg](https://ffmpeg.org), and added it to Systemenvironment variables (PATH)*

*If you are having errors/problems with starting delete the package.json file and do, before you install the packages `npm init`*

<br/>
  
***

## [Discord Server 😎](https://discord.gg/milrato) | [Website](https://milrato.dev)
<a href="https://discord.gg/milrato"><img src="https://discord.com/api/guilds/773668217163218944/widget.png?style=banner2"></a>

***

## SUPPORT ME AND MILRATO DEVELOPMENT

> You can always Support me by inviting one of my **own Discord Bots**

[![2021's best Music Bot | Lava Music](https://cdn.discordapp.com/attachments/748533465972080670/817088638780440579/test3.png)](https://lava.milrato.dev)
[![Musicium Music Bot](https://cdn.discordapp.com/attachments/742446682381221938/770055673965707264/test1.png)](https://musicium.musicium.dev)
[![Milrato Multi Bot](https://cdn.discordapp.com/attachments/742446682381221938/770056826724679680/test1.png)](https://milrato.milrato.dev)

# Credits

> If consider using this Bot, make sure to credit me!
