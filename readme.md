## WhatsApp Bot In Javascript Baileys Web API

<p>Xstro is a simple WhatsApp bot I made to make using WhatsApp faster and easier. It fully depends on the XSTRO API where all the functionality is processed. I used Axios to keep it lightweight and fast. All you need is a decent internet connection from your server.
Powered By Baileys Open Source WhatsApp Web API</p>

## SETUP

### Fork the Repo

First, Fork your own copy of the repo to your GitHub account.

[![FORK REPO](https://img.shields.io/badge/FORK_REPO-100000?style=for-the-badge&logo=github&logoColor=white&labelColor=black&color=black)](https://github.com/AstroX11/Xstro/fork)

### Get a Session

Get Session ID from render server.

[![GET SESSION](https://img.shields.io/badge/GET_SESSION-100000?style=for-the-badge&logo=render&logoColor=white&labelColor=black&color=black)](https://bit.ly/41mQBbY)

### NOTICE

I’m not responsible for you messing around and getting your account banned. As long as you don’t modify the source code to fit your idiotic needs, you’re fine. But seriously, don’t go spamming others. I’m tired of repeating this.

### DEPLOYMENT PLATFORMS

#### Deploy to Render

1. Create an account on Render if you don’t already have one.

[![Create Render Account](https://img.shields.io/badge/-Create-black?style=for-the-badge&logo=render&logoColor=white)](https://dashboard.render.com/register)

2. Get your **DATABASE_URL** from the [Render Dashboard](https://dashboard.render.com/new/database) and copy it.

3. Now you can deploy.

[![Deploy to Render](https://img.shields.io/badge/-DEPLOY-black?style=for-the-badge&logo=render&logoColor=white)](https://render.com/deploy?repo=https://github.com/AstroX11/Xstro)

#### Heroku Deployment

1. Create an account on Heroku if you don’t have one.

[![Create Heroku Account](https://img.shields.io/badge/-Create-black?style=for-the-badge&logo=heroku&logoColor=white)](https://signup.heroku.com/)

2. Setup Application

[![Deploy to Heroku](https://img.shields.io/badge/-Deploy-black?style=for-the-badge&logo=heroku&logoColor=white)](https://www.heroku.com/deploy?template=https://github.com/AstroX11/Xstro)

3. On Heroku make sure to to choose worker as runtime else the application would crash, I don't know how to support heroku web, it's not my code it's their platform.

#### Koyeb Deployment

1. Create an account on Koyeb, make sure to use a 1 year old Gmail/Outlook Account else you will ban instantly.

[![Create Koyeb Account](https://img.shields.io/badge/-Create-black?style=for-the-badge&logo=koyeb&logoColor=white)](https://app.koyeb.com/auth/signup)

2. Get your **_DATABASE_URL_** from Koyeb or Render, I'm not going to provide tutorial on that, ask in the community

3. Deploy the bot.

[![Deploy to Koyeb](https://img.shields.io/badge/-DEPLOY-black?style=for-the-badge&logo=koyeb&logoColor=white)](https://app.koyeb.com/services/deploy/?type=git&repository=https%3A%2F%2Fgithub.com%2FAstroX11%2FXstro&branch=main&name=xstro-bot&builder=dockerfile&dockerfile=.%2Flib%2FDockerfile&ports=3000%3Bhttp%3B%2F&env%5BNODE_ENV%5D=production&env%5BSESSION_ID%5D=&env%5BSUDO%5D=2348039607375&env%5BCMD_REACT%5D=true&env%5BBOT_INFO%5D=Astro%3BXstro-Md%3B&env%5BMODE%5D=private&env%5BAUTO_STATUS_READ%5D=false&env%5BAUTO_READ%5D=false&env%5BSTICKER_PACK%5D=Astro%3BXstro&env%5BPREFIX%5D=.&env%5BLOGS%5D=false&env%5BPORT%5D=3000)

#### Windows Support

#### 1. Install Node.js

NodeJs is the core of this project, not installing it on windows make you dumb, so in order to have nodejs download this version I used to build Xstro from [Here](https://nodejs.org/dist/v22.12.0/node-v22.12.0-x64.msi).

#### 2. Installation

Once you have setup NodeJs make sure to restart your pc, then install [git](https://git-scm.com/download/win), once done copy the following below and paste in powershell.

```bash
npm i -g pm2 yarn
git clone https://github.com/AstroX11/Xstro.git
cd Xstro
yarn install
```

#### 3. Configuration

If you don't trust the terminal (noobs) then go to the folder where the git file was downloaded to and create a file named `.env` once you have done that copy the line below and paste in there, remove `echo` from the line and edit the vars.

```bash
echo "SESSION_ID=null
CMD_REACT=true
BOT_INFO=Astro;Xstro-Md;
MODE=public
AUTO_STATUS_READ=true
AUTO_READ=true
STICKER_PACK=Astro;Xstro
PREFIX=./," > config.env
```

#### 4. Start the Bot

```bash
npm start
```

#### 5. Stop the Bot

```bash
npm stop
```

### DEVLOPMENTS && TESTING

#### Understanding the Structure

Xstro has a simple structure for managing complex data, I have built a custom Seralization and Class Instance to manage messages [Object] from baileys, check out the `Base.js` and `message.js` to see more details of the structure.

#### Sending Messages Simplifed

```javascript
import Message from './Base.js';

const Instance = new Message(sock, messages);

// Sending Text
Instance.send('Hello World!', { ...miscOptions });

// Sending Image
const imageBuffer = Buffer.from('<ImageBuffer>');
Instance.send(imageBuffer, { ...miscOptions });

// Sending Video
const videoBuffer = Buffer.from('<VideoBuffer>');
Instance.send(videoBuffer, { ...miscOptions });

// Sending Audio
const audioBuffer = Buffer.from('<AudioBuffer>');
Instance.sendAudio(audioBuffer, { ...miscOptions });

// Sending Document
const docBuffer = Buffer.from('<DocumentBuffer>');
Instance.sendDocument(docBuffer, { ...miscOptions });

// Sending Sticker
const stickerBuffer = Buffer.from('<StickerBuffer>');
Instance.sendSticker(stickerBuffer);
```

#### Misc Options?

There are so many misc options, you can check them out from [here](https://github.com/WhiskeySockets/Baileys/blob/master/src/Types/Message.ts) and [here](https://github.com/AstroX11/Xstro/blob/44449ea436b15fb97ab0289d421be8e79f7df4d9/lib/Base.js#L139)

```javascript
const miscOptions = {
    caption: '',
    contextInfo: {
        ...opts, ...opts
    },
    quoted: ...opts
}
```

## CONTRIBUTING

If you want to help out or contribute to the project, feel free to fork the repo and create a pull request. Just don’t break anything.

[![Contribute](https://img.shields.io/badge/CONTRIBUTE-black?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AstroX11/Xstro/blob/master/.github/contributing.md)

[![Join WhatsApp Group](https://img.shields.io/badge/Join_WhatsApp-black?style=for-the-badge&logo=whatsapp&logoColor=white)](https://chat.whatsapp.com/HIvICIvQ8hL4PmqBu7a2C6)
