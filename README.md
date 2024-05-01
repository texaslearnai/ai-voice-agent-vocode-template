# AI Voice Agent

This AI Voice Agent is designed and built  to provide an advanced telephony interface using Vocode's telephony server. 

## Setup Manual

To set up the AI Voice Agent, follow these steps:

1. Sign up to [Github](https://github.com).
2. Fork [repository](https://github.com/texaslearnai/ai-voice-agent-vocode-template) under your own Github account
3. Sign up to [OpenAI](https://openai.com). Create an API Key and store it somewhere.
4. Sign up to [deepgram](https://deepgram.com). Create an API Key and store it somewhere.
5. Go to [webhook.site](https://webhook.site)
6. Sign up to [Twilio](https://twilio.com).
7. Sign up to [Render](https://render.com).
8. Navigate to "New" > "Web Service" and connect your GitHub account if you haven't done that yet.
9. Once done, Render will automatically set most of the values for you. You can customize the Region as you wish.
10. Set the following environment variables: 
    - `OPENAI_API_KEY`: Set this to your OpenAI API key.
    - `TRANSCRIPT_CALLBACK_URL`: Set this to the webhook.site URL you want to call once a call was completed.
    - `TWILIO_ACCOUNT_SID`: Your Twilio Account ID.
    - `TWILIO_AUTH_TOKEN`: Your Twilio Auth token.
    - `DEEPGRAM_API_KEY`: The API key for your Deepgram Acccount.
11. Once the app is deployed successfully, copy the Render.com URL and add `/inbound_call` at the end of it
12. Paste that URL into the Webhook field of your Twilio Phone Number

## Manual Installation

This part of the manual is intended if you run the installation locally.

First, build the application using Docker:

```docker build -t shiva-telephony-app .```

Then, run the application using docker-compose. From the `telephony_app` directory, run:

```docker-compose up```


## Vocode Self-hosted Telephony Server

For a more detailed guide on setting up the telephony server, visit [Vocode's official documentation](https://docs.vocode.dev/open-source/telephony).

See [Vocode's Self-hosted Telephony Setup](https://docs.vocode.dev/telephony#self-hosted) for detailed setup steps!
