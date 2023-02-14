chatgpt_telegram_bot

This repository contains the code for a Telegram bot that leverages OpenAI's GPT-3 API to generate natural language responses. The bot is written in Python and uses the Flask web framework to handle incoming requests from Telegram's bot API. The result is a fast and reliable experience, with response times usually taking only 3-5 seconds.

Key Features

1. Rapid response times
2. No limitations on the number of requests
3. Syntax highlighting for code snippets
4. Custom chat modes, including Personal Assistant and Code Assistant
5. Whitelist of authorized Telegram users
6. Monitoring of API usage costs using the OpenAI API


Bot Commands

/retry - Regenerates the previous bot response
/new - Initiates a new conversation
/mode - Selects the chat mode
/balance - Displays current usage costs
/help - Displays a help prompt

Deployment

1. Obtain an OpenAI API key
2. Acquire a Telegram bot token from @BotFather
3. Customize config/config.example.yml with your tokens, then run the following commands (experienced users may also edit config/config.example.env):
"
mv config/config.example.yml config/config.yml
mv config/config.example.env config/config.env
"
4. Finally, lauch the deployment 
"
docker-compose --env-file config/config.env up --build
"

Docker

1. In order to run the project in a Docker container, you will need to add the following steps to the deployment process:

Install Docker on your machine

1. Run the following commands in the project root directory:
"
RUN python -m pip install --upgrade pip
RUN pip3 install -r requirements.txt --root-user-action=ignore
ENV PIP_ROOT_USER_ACTION=ignore
"

