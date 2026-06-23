PixelFlow AI – Telegram Image Generator

PixelFlow AI is an AI-powered Telegram bot that generates images from text prompts. Users can send an image idea directly in Telegram, and the bot generates and returns an AI image within seconds.

Live Demo

🤖 Try the bot: https://t.me/bhargav_pixelflow_ai_bot

Example prompt:

A futuristic cyberpunk city at night with rain

Features

* Generate AI images from Telegram text prompts
* /start welcome message and /help command
* “Generating your image…” status message
* Re-Generate button for a new variation of the same prompt
* Generate More button for a new image request
* Help button with prompt-writing tips
* User-specific prompt storage using Telegram chat ID
* Random seed-based image variations
* Prompt enhancement for better image quality

Tech Stack

* Telegram Bot API – User interface and image delivery
* n8n Cloud – Workflow automation and backend logic
* Pollinations AI – AI image generation API
* Google Sheets – Stores each user’s latest prompt
* HTTP Request API – Connects n8n with the image generation API

How It Works

User sends prompt on Telegram --> Telegram Trigger receives message --> Prompt is stored in Google Sheets with chatId --> n8n calls Pollinations AI Image API --> Generated image is sent back through Telegram

Re-Generate Flow

User clicks Re-Generate --> Bot fetches that user's last prompt using chatId --> Same prompt is sent with a new random seed --> A different image variation is generated

Key Implementation Details

* Telegram chatId identifies each user.
* Google Sheets stores chatId and lastPrompt.
* Re-Generate retrieves only the current user’s last prompt.
* A random seed creates a different image variation for the same prompt.
* Quality keywords such as ultra detailed, cinematic lighting, and sharp focus are automatically added to improve output quality.

Future Improvements

* Add style buttons: Realistic, Anime, 3D, Cinematic
* Add user image history
* Replace Google Sheets with MongoDB/PostgreSQL
* Add rate limiting and error handling
* Integrate premium models such as FLUX or Imagen
