# chatgpt-api-boilerplate

Chat GPT API boilerplate

## What do you need
1. Register an open AI account at https://platform.openai.com/, you can also use your Google Workspace login to do that.
1. Setup billing (it's not free) by going to https://platform.openai.com/account/billing/overview and link your credit card.
1. Generate yourself an API key here https://platform.openai.com/account/api-keys

## How to use - curl
If you just want to try it out without installing anything, just do the following in the terminal. 
```
export OPENAI_API_KEY=<replace with your api key>

curl https://api.openai.com/v1/chat/completions \
 -H "Authorization: Bearer $OPENAI_API_KEY" \
 -H "Content-Type: application/json" \
 -d '{
 "model": "gpt-3.5-turbo",
 "messages": [{"role": "user", "content": "What is the OpenAI mission?"}] 
 }'
```

If you want to use the Python SDK do
```
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

export OPENAI_API_KEY=<replace with your api key>
python main.py
```

See more docs, see https://openai.com/blog/introducing-chatgpt-and-whisper-apis
