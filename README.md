# Smart FAQ Builder

Product URL → 20 real-customer FAQs with objection-handling answers + schema markup

## Overvew
Takes any product URL and generates benefit-oriented FAQs that anticipate 
real customer concerns. Outputs are ready for SEO, Shopify, and chatbot use.

## Inputs
- `product_url` (required) — any public product page URL
- `faq_count` — number of FAQs to generate (10–30, default 20)
- `tone` — writing tone (professional, friendly, casual, etc.)
- `language` — output language (default English)
- `question_sources` — sources to draw questions from
- `competitor_comparison` — include comparison FAQs (true/false)

## Outputs
- `faqs` — full FAQ array with question, answer, theme
- `json_ld` — JSON-LD schema markup for Google rich snippets
- `shopify_html` — drop-in HTML block grouped by theme
- `chatbot_csv` — CSV formatted for chatbot training
- `objection_faqs` — subset targeting price/returns/warranty/delivery

## Stack
n8n · Ollama Mistral · Web scraping · Schema generator

## How to run
1. Import `n8n.json` into your n8n instance
2. Setup Ollama
3. Set the Webhook node → Respond → "Using Respond to Webhook Node"
4. Activate the workflow
5. POST to the webhook URL with a JSON body matching `input_form.json`
