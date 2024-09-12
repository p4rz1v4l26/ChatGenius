# ChatGenius - ChatGPT Youtube Bot

Welcome to the ChatGPT Youtube Bot setup guide! This Node.js Chat Bot integrates seamlessly with ChatGPT, providing prompt responses and engaging conversations. Below is a step-by-step guide on how to set up and customize your own version of the bot.

## 1. Fork this on Github

Start by logging into your Github account and forking this repository. <strong>Don't forget to give it a star too!</strong>

---

## 2. Fill out your context file

Open the file named `file_context.txt` and fill it with background information for ChatGPT. This information enhances the bot's responses. Feel free to provide any details you think would be helpful for training your bot.

(I made This Template for my friend [FleXGuy](https://www.youtube.com/channel/UCjx7TNunoyeub4E2zhBky2Q) ..Feel free to add or remove any info from the template)

---

## 3. Create an OpenAI account

Visit [OpenAI's platform](https://platform.openai.com) and create an account. Initially, you'll have a free usage limit, but later on, you may need to pay for server usage. You can set a spending limit in your account settings to manage costs.

---

## 4. Get your OpenAI Secure Key

In your OpenAI account, navigate to the API keys section and generate a new secret key. Keep this key safe, as it will be used to authorize your bot with OpenAI. Treat it like the key to your wallet.

---

## 5. Deploy this repo on Render or any service provider

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy)
Click the button to deploy this repository on Render or choose any other service provider you prefer. Log in with your Github account and select your repository for deployment.

---

## 6. Set your environment variables

After deployment, set up three environment variables in your deployment settings:

### GPT_MODE

Choose between two values:

- **"CHAT"**: Chat mode with history. It's cheaper than prompt mode but faster. Uses the `gpt-3.5-turbo` model.
- **"PROMPT"**: Prompt mode with no history. Uses the `text-davinci-003` model.

### HISTORY_LENGTH

This variable only works when GPT_MODE is set to "CHAT". Enter a number to define how many bot-user conversations will be saved and sent along with the most recent user message. This allows ChatGPT to remember context and engage in conversations.

### OPENAI_API_KEY

Paste your OpenAI Secure Key here.

---

## 7. Get your API Link from Render

Copy the API link provided by Render after deployment. You can find it in the top-left corner below the title of your deployed repository.

---

## 8. Add your API Command to your Chatbot

Now, let's integrate your Chat Command:

### Nightbot

Go to your Nightbot commands page and add a new command. Enter the following message:

```bash
$(urlfetch https://your-Render-url.app/gpt/"$(user):$(querystring)")
```

Replace "your-Render-url.app" with the API link you copied earlier.

## Contributing

as always Contributions to this project are welcome! If you have any suggestions or improvements, feel free to open an issue or submit a pull request.

## Contact

If you have any questions or inquiries, please feel free to get in touch:

- Email: avinash.warale@yandex.com
- Discord: [@p4rz1v4l26](https://discordapp.com/users/896411007797325824/)

or you can join

- [Discord server](https://discord.gg/vFWB2KGcH9)
