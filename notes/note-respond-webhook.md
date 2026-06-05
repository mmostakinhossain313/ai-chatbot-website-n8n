# Respond to Webhook Note

This node sends the AI answer back to the website visitor.

Without this node, the visitor gets no response.
The chatbot just hangs and nothing appears.

Settings I use:
- Respond With: Text
- Response Body: {{ $json.output[0].content[0].text }}
- Expression toggle: ON

I also must set the Webhook node to:
Respond = "Using Respond to Webhook Node"
Otherwise this node never runs.

One mistake I made:
I used JSON mode instead of Text.
The HTML could not read JSON properly.
Switched to Text and everything worked perfectly.
