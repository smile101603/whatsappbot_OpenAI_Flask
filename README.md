# WhatsApp Chatbot with AI

This project implements a chatbot for WhatsApp using the WhatsApp Business API, Flask for the backend, and OpenAI's AI for natural language processing.

## Project Architecture

The system consists of several key components that work together to provide an interactive experience through WhatsApp:

- Flask Server: Handles HTTP requests and serves as the connection point between WhatsApp and the AI ​​engine.

- WhatsApp Business API: Enables receiving and sending messages through WhatsApp.

- OpenAI API: Used to generate intelligent responses from received questions.

- Google Cloud Storage: Stores and manages the keywords for the AI.

When a message arrives via WhatsApp, Flask processes the request, passes it to the OpenAI API to generate a response, and then uses the WhatsApp Business API to send this response to the user.

[![WhatsApp AI Chatbot Architecture](whatsapp-ai-chatbot-architecture.png)](https://github.com/smile101603/whatsappbot_OpenAI_Flask/blob/main/whatsapp-ai-chatbot-arquitectura.png)

### Prerequisites

To run this project you need:

- A Google Cloud account for vector storage.

- A Facebook developer account with access to the WhatsApp Business API.

- Access to the OpenAI API.

### Project Configuration

Environment Variables: Configure the following environment variables on your system or in an .env file:

- WHATSAPP_ACCESS_TOKEN: Your access token for the WhatsApp Business API.

- WHATSAPP_VERIFY_TOKEN: Your verification token for the WhatsApp Business API.

- WHATSAPP_API_URL: The URL of the WhatsApp Business API.

- OPENAI_SERVICE_URL: The URL of your service that interacts with the OpenAI API.

- GOOGLE_APPLICATION_CREDENTIALS: The path to your Google Cloud account credentials file.

**Installing Dependencies: Run `pip install -r requirements.txt` to install the necessary dependencies.**

#### Local Execution:

- Start the Flask server with `python app.py`.

- Ensure that the ports and callback URLs are correctly configured in your WhatsApp and OpenAI services.

#### Deployment

- To deploy this bot, you can use services such as Heroku, AWS, or Google Cloud. Make sure to configure the environment variables on your deployment platform.

- Once the bot is up and running, it will be able to interact with users via WhatsApp, answer questions, and provide information using OpenAI's artificial intelligence.
