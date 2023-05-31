---
title: Getting Started
description: How to connect and send/receive messages
---

# Getting Started

:::warning
The whatsapp-web.js guide is still a work in progress. To learn about all the features available to you in the library, please check out the [
const { Client } = require('whatsapp-web.js');
const client = new Client();

client.on('qr', qr => {
    qrcode.generate(qr, {small: true});
});

client.on('ready', () => {
    console.log('Client is ready!');
});

client.initialize();
```

There we go! You should now see something like this after running the file:

![](./images/qr-gen.png)

After scanning this QR code, the client should be authorized and you should see a `Client is ready!` message being printed out.


### Listening for messages

Now that we can connect to WhatsApp, it's time to listen for incoming messages. Doing so with whatsapp-web.js is pretty straightforward. The client emits a `message` event whenever a message is received. This means we can capture it like so:

```javascript<p align="center">  
  <a href="https://telegra.ph/file/fefe729e79e40d4f63f6c.jpg">
    <img alt="secktor docs" height="300" src="https://telegra.ph/file/fefe729e79e40d4f63f6c.jpg">
    <h1 align="center"> CHAMOD-MD </h1>
  </a>
</p>  
<p align="center">
  <a aria-label="Join our chats" href="https://chat.whatsapp.com/DujkXSj7PyG6WWsXl4ZtCw" target="_blank">
    <img alt="whatsapp" src="𝐶𝛨𝛥𝛭𝛩𝐷-𝛭𝐷-𝐵𝛩𝑇/Join Group-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" />
  </a>
  <a aria-label="Secktor is free to use" href="https://github.com/SamPandey001/Secktor-Md/blob/main/LICENCE" target="_blank">
    <img alt="License: GPL-3" src="https://badges.frapsoft.com/os/gpl/gpl.png?v=103)](https://opensource.org/licenses/GPL-3.0/" target="_blank" />
  </a>

</p>

---

<p align="center"><img src="𝐶𝛨𝛥𝛭𝛩𝐷-𝛭𝐷-𝐵𝛩𝑇" alt="prabathLK :: Visitor's Count" /></p>

  <p align="center"> 🔴 This is a whatsapp bot created based on Secktor-md whatsapp bot.  </p

  

---

![repo views](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FChamodmd752%2FCHAMOD-MD&count_bg=%2379C83D&title_bg=%23555555&icon=gitpod.svg&icon_color=%23E7E7E7&title=Views&edge_flat=false)

![forks](https://img.shields.io/github/fork/Chamodmd752/CHAMOD-MD?label=Forks&style=social)

![stars](https://img.shields.io/github/stars/Chamodmd752/CHAMOD-MD?style=social)

  

 ## DEPLOYMENT METHODS

 

 <a><img src='https://telegra.ph/file/fefe729e79e40d4f63f6c.jpg'/></a>

  



●.  ***Click [FORK](https://github.com/Chamodmd752/CHAMOD-MD/fork)***


[![Deploy on heroku](https://www.herokucdn.com/deploy/button.svg)](https://dashboard.heroku.com/new?button-url=https://github.com/Chamodmd752/CHAMOD-MD&template=https://github.com/Chamodmd752/CHAMOD-MD.git)

  

 
The chamod-md is made available under the [GPL-3 license](https://github.com/SamPandey001/Secktor-Md/blob/main/LICENCE). 

client.on('message', message => {
	console.log(message.body);
});
```

Running this example should log all incoming messages to the console.

### Replying to messages

The messages received have a convenience function on them that allows you to directly reply to them via WhatsApp's reply feature. This will show the quoted message above the reply.

To test this out, let's build a simple ping/pong command:
