# Common Errors I Faced — AI Chatbot

Error 1: 404 Webhook Not Registered
Reason: I used Test URL in production.
Fix: Always use Production URL after publishing.

Error 2: JSON Syntax Error in Browser
Reason: Used response.json() but n8n sends plain text.
Fix: Change response.json() to response.text()

Error 3: Chatbot sends question but no answer comes back
Reason: Respond to Webhook node was not connected.
Fix: Connect OpenAI node to Respond to Webhook node.

Error 4: Expression shows as plain text
Reason: Expression toggle was off.
Fix: Click the expression button next to the field.

Error 5: CORS Error on local file
Reason: Cannot call external APIs from local HTML file.
Fix: Host on GitHub Pages. Free and instant.

Error 6: Empty answer in chatbot
Reason: Wrong data path in Response Body.
Fix: Use {{ $json.output[0].content[0].text }}
