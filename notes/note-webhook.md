# Webhook Note

I use Webhook when there is no app trigger available.
For example, a website contact form or a custom chatbot.

The Webhook sits and waits for data to arrive.
The moment data comes in, the workflow starts.

Two URLs exist in n8n:
- Test URL — only works when I click "Listen for test event"
- Production URL — works always after publishing

I always use Production URL in the final product.
I always use Test URL only while building.

HTTP Method must be POST when sending JSON data.

One mistake I made:
I used Test URL in the HTML file.
The chatbot stopped working after I closed n8n.
Always use Production URL in any external app or website.
