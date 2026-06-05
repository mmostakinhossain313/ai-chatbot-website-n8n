# HTML Chatbot Note

I built a simple chatbot UI using HTML and JavaScript.
No framework needed. No backend needed.
Just one HTML file.

The chatbot sends questions to the n8n Webhook URL.
The Webhook processes it through OpenAI.
The answer comes back and shows in the chat box.

Important code line:
const data = await response.text();

I must use response.text() not response.json()
Because n8n sends plain text, not JSON.

One mistake I made:
I used response.json() at first.
Got a syntax error in the browser console.
Switched to response.text() and it worked instantly.

I hosted the HTML file on GitHub Pages.
This is important because:
Local files cannot talk to external APIs (CORS error).
GitHub Pages is free and solves this completely.

Live URL format:
https://username.github.io/repository-name/chatbot.html
