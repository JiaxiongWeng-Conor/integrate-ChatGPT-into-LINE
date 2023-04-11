# Integrating-ChatGPT-into-Discord

### Introduction:

In today's fast-paced world, it is crucial to have quick and efficient access to information. As the consumption of video content continues to grow exponentially, finding a way to extract key information from these videos becomes increasingly important. This guide will explore the innovative integration of ChatGPT with Apple's Siri voice assistant, focusing on the automatic generation of video content summaries. By combining the advanced language processing capabilities of ChatGPT with Siri's user-friendly voice interface, we unlock a powerful solution for streamlining information retrieval.

### Steps for Integrating ChatGPT into Discord

**Step 1 Create an account/login to account** [ChatGPT Website](https://chat.openai.com/auth/login)
1. When using chatGPT for the first time, go to the chatGPT website to create an account

![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrating-ChatGPT-to-siri/blob/f1d2e83ecaab9697e5c99dbefbf21963fa44e586/Image/WX20230324-143335.png)

2. Click on "Sign up" to register account, or "Log in" if you have one.

![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrating-ChatGPT-to-siri/blob/f1d2e83ecaab9697e5c99dbefbf21963fa44e586/Image/WX20230324-143253.png)

**Step 2 Access to ChatGPT API**
1. Once logged in, go to this website for API claims:(https://platform.openai.com/account/api-keys)
2. Login to account and click on "Create New Security Key" to create the API key.

![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrating-ChatGPT-to-siri/blob/4adb3d68c622b29b0963f103fb00953b836b82b0/Image/WX20230324-144724.png)
**Notice:** 

1）The key will only be displayed once!!! Remember to keep it safe! If the key is not saved in time, it will have to be recreated!

2）Every API comes with limited free quota, for details please see [API documentation](https://openai.com/pricing).

**Step 3 To obtain a Discord token:**

1. Log in to the [Discord Developer portal](https://discord.com/developers/applications).

2. Click on the "New Application" button in the top right corner and enter the name of bot in the provided field.
![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrate-ChatGPT-into-Discord/blob/5f5113de6c78d9d2cbb7940b8600645a3a44f030/Picture/WX20230410-165444@2x.png)
![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrate-ChatGPT-into-Discord/blob/44d472a7266a8f7c432f0ef480a6ee0b93c1e2ea/Picture/WX20230410-165931@2x.png)

3. Click on the "Bot" tab on the left-hand side and then click the "Add Bot" button to create a bot for application.
![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrate-ChatGPT-into-Discord/blob/44d472a7266a8f7c432f0ef480a6ee0b93c1e2ea/Picture/WX20230410-170435@2x.png)
![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrate-ChatGPT-into-Discord/blob/44d472a7266a8f7c432f0ef480a6ee0b93c1e2ea/Picture/WX20230410-170519@2x.png)

4. Scroll down to the "Token" section and click on the "View Token" button to reveal the token.
![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrate-ChatGPT-into-Discord/blob/44d472a7266a8f7c432f0ef480a6ee0b93c1e2ea/Picture/WX20230410-170621@2x.png)
![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrate-ChatGPT-into-Discord/blob/c16070182b596282737af924869e06cafdc60d0a/Picture/WX20230410-170714@2x.png)

5. Scroll down to the "Privileged Gateway Intents" section and toggle on the "Message Content" intent. And then, click on the "Save Changes" button to save your changes.
![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrate-ChatGPT-into-Discord/blob/c16070182b596282737af924869e06cafdc60d0a/Picture/WX20230410-170846@2x.png)

**Step 4 To set up OAuth:**
1. Go to the "OAuth2" section and click on the "URL Generator" option.And then, select "bot" in the "SCOPES" section and select "Administrator" in the "BOT PERMISSIONS" section.
![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrate-ChatGPT-into-Discord/blob/6e18125856374fad7306ced4bc657cecb2121a53/Picture/WX20230410-171141@2x.png)
2. Copy the URL at the bottom of the page and paste it into your web browser.
![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrate-ChatGPT-into-Discord/blob/6e18125856374fad7306ced4bc657cecb2121a53/Picture/WX20230410-171244@2x.png)
4. Select the server you want to add the bot to and click "Continue" and authorize the bot to join the server.
![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrate-ChatGPT-into-Discord/blob/6e18125856374fad7306ced4bc657cecb2121a53/Picture/WX20230410-171428@2x.png)

**Step 5 Fork code from Github**
1. Go to the Integrate-ChatGPT-into-Discord on GitHub.
2. Click on the "Star" button to support the developer.
3. Click on the "Fork" button to copy the code.

**Step 6 Deploy for free**
1. Go to the [Replit](https://replit.com/).
2. Click on the "Sign Up" and sign in with Github account. You can click "Skip" to bypass the initial setup process.
3. On the Replit homepage, click on "Create" in the center of the page. In the pop-up window, click on "Import from Github" in the top right corner.

**Step 7 Run the code**
To set environment variables for your ChatGPT Discord Bot, follow these steps:

1. After importing the code from GitHub, go to the Replit project management page.
2. Click on "Tools" in the bottom left corner of the page and select "Secrets".
3. Click "Got it" to proceed.
4. Add the following environment variables:

OpenAI API Token:
key: OPENAI_API
value: [obtained from step 1] sk-FoXXXX

Selected model:
key: OPENAI_MODEL_ENGINE
value: gpt-3.5-turbo

Role word for ChatGPT to play (currently there are no official instructions on this, players can test it themselves):
key: SYSTEM_MESSAGE
value: You are a helpful assistant.

Discord Token:
key: DISCORD_TOKEN
value: [obtained from step 1] MTA3NXXX

### Support Me with a Cup of Coffee ☕
If you think this small application useful and would like to show your appreciation, please consider buying me a cup of coffee to support my efforts! Your generosity will not only fuel my motivation to continue working on this project, but also help me cover the costs associated with development and maintenance.

To buy me a coffee, simply scan or clik below:

![Github Octocat mascot](https://github.com/JiaxiongWeng-Conor/Integrating-ChatGPT-to-siri/blob/353dc1ae3fdcc5ca2f2e4a8f8c017fddb3a051b1/Image/IMG_6200.jpg)

[Link of venmo](https://account.venmo.com/u/Jiaxiong-Weng)


Thank you for your support! 🙏 
