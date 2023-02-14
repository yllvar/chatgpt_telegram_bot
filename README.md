# chatgpt_telegram_bot
This repository contains the code for a Telegram bot that uses OpenAI's GPT-3 API to generate responses in natural language. Written in Python and uses the Flask web framework to handle incoming requests from Telegram's bot API.

This repository presents a reimplementation of ChatGPT using the GPT-3.5 LLM model as a Telegram Bot. The result is a fast and reliable experience.

Key Features
1. Rapid response times, with replies usually taking only 3-5 seconds
2. No limitations on the number of requests
3. Syntax highlighting for code snippets
4. Custom chat modes: including Assistant, Code Assistant, and Movie Expert, with more to come
5. Whitelist of authorized Telegram users
6. Monitoring of API usage costs using the OpenAI API

Bot Commands
/retry - Regenerates the previous bot response
/new - Initiates a new conversation
/mode - Select the chat mode
/balance - Display current usage costs
/help - Display a help prompt

Deployment
1. Obtain an OpenAI API key

2. Acquire a Telegram bot token from @BotFather

3. Customize config/config.example.yml with your tokens, then run the following commands (experienced users may also edit config/config.example.env):
"
mv config/config.example.yml config/config.yml
mv config/config.example.env config/config.env
"

4. Finally, launch the deployment:
"
docker-compose --env-file config/config.env up --build
"

Additional Resources
1. Build ChatGPT from GPT-3
