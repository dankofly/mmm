# Claude + Remotion Video Generation

**Source:** Sabrina Ramonov — "Claude + Remotion Unlocks UNLIMITED Cheap Video Generation"

## Setup

```bash
npx skills add remotion-dev/skills
claude
```

## 5 Video Templates

### 1. Education Explainer Videos

**Input:** Topic in quotes (e.g., "How AI Agents Work")
**Output:** 30-second vertical video with SVG diagrams and motion graphics
**Specs:** 1080x1920, 30fps, spring animations with staggered timing

```
Use the Remotion best practices skill. Create a 30-second vertical education explainer video about "[YOUR TOPIC]". Research the topic, write a script, design 5 scenes with SVG diagrams and motion graphics. Dark background, spring animations, staggered timing. No walls of text — dense information, beautiful motion, fast pacing. 1080x1920, 30fps.
```

### 2. Product Demo + Launch Videos

**Input:** Product URL
**Output:** 25-second video with animated UI interaction + real screenshots

```
Use the Remotion best practices skill. Create a 25-second product demo video for [PRODUCT URL]. Scrape the branding and download product images. Scene 1: pain-point hook. Scene 2: feature callouts. Scene 3: cursor animations clicking through simplified product UI. Display downloaded product images at near-full width (900px+). Use real screenshots, not mockups.
```

### 3. Google Reviews Testimonials

**Input:** Google Business Profile link
**Output:** 20-second social proof video with animated star ratings

```
Use the Remotion best practices skill. Create a 20-second testimonial video from this Google Business Profile: [LINK]. Scrape real reviews, ratings, and business info. 5 large star SVGs fill in one by one from left to right with gold color (#f59e0b). Light background (#f8f9fa). Review carousel with spring transitions.
```

### 4. Avatar + Animated Overlays

**Input:** 9:16 talking-head video at public/avatar.mp4
**Output:** Original video with animated overlay graphics synced to speech

```
Use the Remotion best practices skill. Take the talking-head video at public/avatar.mp4. Transcribe the speech. Overlay animated titles, topic badges, keyword pills, and captions on the TOP 35% of the frame only (above subject's head). Large faded step numbers ("01", "02") for each topic. Keep original video full-frame. Do not crop or resize the source video.
```

### 5. Data Visualization Dashboards

**Input:** CSV file at public/data.csv
**Output:** 15-second vertical dashboard with animated charts

```
Use the Remotion best practices skill. Analyze the CSV data at public/data.csv. Select appropriate chart types (bar, donut, line). Create a 15-second vertical dashboard video with KPI cards, animated bar charts (spring growth), donut charts, line graphs (stroke-dashoffset draw). Values count up using interpolate(). Stagger animations by 8-12 frames.
```

## Universal Design Rules

**Safe Zones:**
- 150px from top (status bars)
- 170px from bottom (navigation)
- 60px side margins

**Font Sizes:** 56px headlines, 36px body, 28px labels

**Animations:**
- `spring({ damping: 200 })` for entrances
- Stagger related items by 8-12 frames
- `TransitionSeries` with 12-frame fades
- `interpolate()` with `clamp()` for count-ups

**Typography:** Inter (400, 600, 700, 800), Roboto Mono for monospace

## Iteration Workflow

1. Paste prompt with "Use the Remotion best practices skill"
2. Claude generates script/layout for approval
3. Claude builds the composition
4. Preview: `npx remotion studio`
5. Refine with follow-up prompts

---

# 11 Free AI Courses with Certificates

| # | Course | Provider | Cost |
|---|--------|----------|------|
| 1 | AI for Everyone: Master the Basics | IBM/edX | Free |
| 2 | AI Fundamentals | IBM Skills Build | Free |
| 3 | Elements of AI | University of Helsinki | Free |
| 4 | AI & Career Empowerment | UMD Smith School | Free |
| 5 | AI for Business Professionals | HP/Life Global | Free |
| 6 | AI for Everyone | DeepLearning.AI | $49 cert |
| 7 | Generative AI Leader | Google Cloud | $99 exam |
| 8 | Career Essentials in Gen AI | Microsoft/LinkedIn | Free w/ Premium |
| 9 | Human Skills in Age of AI | Microsoft/LinkedIn | Free w/ Premium |
| 10 | AI for Organizational Leaders | Microsoft/LinkedIn | Free w/ Premium |
| 11 | AI for Managers | Microsoft/LinkedIn | Free w/ Premium |
