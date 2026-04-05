# AI Social Media System

**Source:** Sabrina Ramonov — "I Built an AI Social Media System"

Fully automated system: article in → platform-specific posts out across all social media.

## Tools Required

- **Make.com** — workflow orchestration
- **Google Sheets** — content input trigger
- **OpenAI API** — text extraction + content generation
- **DALL-E 3** — image generation
- **HeyGen** — AI avatar video creation
- **Blotato** ($29/mo) — multi-platform publishing API

## Workflow

```
Google Sheets (new article URL)
    |
    v
HTTP Module (fetch raw article)
    |
    v
OpenAI (extract clean text from HTML)
    |
    v
OpenAI (write platform-specific posts)
    |
    ├── Twitter/Threads: text-only posts
    ├── LinkedIn/Facebook/Instagram: text + DALL-E images
    └── TikTok: AI avatar video (HeyGen)
    |
    v
Blotato API (publish to all platforms simultaneously)
```

## Setup

1. Create Make.com scenario
2. Configure Google Sheets trigger (watch for new rows)
3. Add HTTP module to fetch article content
4. Add OpenAI module for text extraction
5. Add OpenAI module for platform-specific post generation
6. Add DALL-E module for image generation
7. Add HeyGen module for video creation
8. Add Blotato HTTP module for publishing

## Note

Best for intermediate/advanced creators with established voice. For evergreen content, lead magnets, and breaking news. Not recommended for beginners still developing their voice.

---

# AI Avatar Clone System

**Source:** Sabrina Ramonov — "Your 100% Automated AI Clone Makes Talking Videos"

Daily automated video creation: research → script → avatar video → publish.

## Tools Required

- **Make.com** — daily scheduling + orchestration
- **Perplexity API** — real-time research + script generation
- **ChatGPT API (GPT-4o mini)** — caption creation
- **HeyGen API** — avatar video production
- **Blotato** ($29/mo) — multi-platform publishing

## Script Generation Prompt (Perplexity)

Key requirements:
- Research the internet for current information
- 6th-grade reading level
- 25-second monologue
- Negative hook opening ("don't miss this", "if you're not doing this")
- Zero formatting artifacts (critical for avatar voice synthesis)

## Caption Prompt (ChatGPT)

Generate 50-word captions:
- One summarizing paragraph
- Three search-engine relevant questions
- Five hashtags
- Active voice, no adjectives/adverbs
- Same banned word list as humanize prompt

## HeyGen Setup

1. Record 5 minutes of continuous video (smartphone OK)
2. No excessive gestures or stitched clips
3. Consistent, unedited material
4. Video dimensions: 720x1280 (vertical)
5. Wait 5 min for videos under 30 sec

## Publishing

Blotato API distributes to: Instagram, TikTok, LinkedIn, Twitter, Facebook, Threads simultaneously.

## Critical Tips

- Manually review scripts before full automation
- Test all modules independently first
- HeyGen rejects stitched/edited footage
- Schedule Make scenarios daily
