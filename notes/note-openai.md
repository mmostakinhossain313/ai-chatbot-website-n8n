# OpenAI Note

OpenAI node is the brain of the AI chatbot.

Model I use: gpt-4o-mini
It is fast. It is smart. It is cheap.
Perfect for small business chatbots.

Two important fields:

System Prompt — this tells the AI who it is.
Example:
"You are a helpful customer support assistant.
Answer questions politely and professionally.
Keep answers short and clear.
If you do not know, say please contact us directly."

User Prompt — this is the visitor's question.
I map it from the Webhook like this:
{{ $json.body.question }}

One mistake I made:
I forgot to turn on Expression toggle.
The question was sent as plain text, not as a variable.
Always turn on Expression before mapping any field.
