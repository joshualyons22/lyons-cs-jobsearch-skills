# Portfolio Site — Customization Guide

This guide walks you through every `[PLACEHOLDER]` in the template with examples.

---

## Page Title & Navigation

**Location:** Line ~6 and ~39

### `[YOUR_NAME]`
The page title and nav branding.

```html
<!-- Line 6 (page title) -->
<title>[YOUR_NAME] — AI-Powered CS Workflows</title>

<!-- Line 39 (nav name) -->
<a href="#" class="nav-name">[YOUR_NAME]</a>
```

**Example:**
```html
<title>Sarah Chen — AI-Powered CS Workflows</title>
<a href="#" class="nav-name">Sarah Chen</a>
```

---

## Hero Section — Main Headline & Description

**Location:** Lines ~81-85

### `[YOUR_HERO_DESCRIPTION]`
One or two sentences about your CS approach and AI work. Aim for 1-2 readable sentences.

```html
<h1>I build <em>efficiency</em> into your CS motion</h1>
<p class="hero-desc">[YOUR_HERO_DESCRIPTION]</p>
```

**Example (Joshua's):**
```html
<p class="hero-desc">I turn at-risk accounts into expanding partners and build AI tools that my colleagues actually use. In 18 months at Cloudflare, I protected $4M ARR across 6 high-risk saves, grew a book of 20 Enterprise accounts 20% YoY, and shipped AI-powered workflows adopted across CS and Sales.</p>
```

**Tips:**
- Lead with the outcome, not the process
- Be specific: numbers, ARR amounts, specific tools
- Keep it under 3 sentences for impact

---

## Hero Section — Four Key Statistics

**Location:** Lines ~87-100

These appear as 4 cards in a 2×2 grid. Pick your most compelling metrics.

```html
<div class="hero-stat">
  <div class="hero-stat-number">[STAT_1_NUMBER]</div>
  <div class="hero-stat-label">[STAT_1_LABEL]</div>
</div>
```

**Examples:**
- `100% | Logo retention`
- `$4M | ARR protected (saves)`
- `20% | Annual ARR growth`
- `4hrs | Saved monthly on reporting`

**Tips:**
- Make the numbers big and easy to scan
- Use simple labels (one line max)
- Lead with the most impressive stat

---

## Hero Section — Tool Cards (3 cards)

**Location:** Lines ~105-125

These appear as 2 regular cards + 1 featured (dark navy) card.

### Regular Cards (2)

```html
<div class="tool-card">
  <div class="tool-icon">[TOOL_1_ICON]</div>
  <h3>[TOOL_1_NAME]</h3>
  <p>[TOOL_1_DESC]</p>
  <div class="tool-impact">[TOOL_1_IMPACT]</div>
</div>
```

- `[TOOL_1_ICON]` — Emoji (example: 🎯, 📊, ⚡, 🔗)
- `[TOOL_1_NAME]` — Short tool name (1-3 words)
- `[TOOL_1_DESC]` — One sentence describing what it does
- `[TOOL_1_IMPACT]` — Impact metric (example: "Saves 15 min/call")

**Examples:**

Card 1:
```html
<div class="tool-icon">🎯</div>
<h3>Negotiation Skill</h3>
<p>Black Swan methodology for difficult customer conversations</p>
<div class="tool-impact">Used by 30+ Sales AEs</div>
```

Card 2:
```html
<div class="tool-icon">📊</div>
<h3>Usage Reporting</h3>
<p>Monthly automation replacing manual data pulls</p>
<div class="tool-impact">7+ hours saved monthly</div>
```

### Featured Card (1)

Same structure, but highlighted and spanning full width:

```html
<div class="tool-card featured">
  <div class="tool-icon">[FEATURED_TOOL_ICON]</div>
  <h3>[FEATURED_TOOL_NAME]</h3>
  <p>[FEATURED_TOOL_DESC]</p>
</div>
```

**Example:**
```html
<div class="tool-card featured">
  <div class="tool-icon">⚡</div>
  <h3>Post-Meeting Brief Automation</h3>
  <p>Automated customer-facing briefs replacing 15+ minute manual writes</p>
  <div class="tool-impact" style="color: var(--orange); background: rgba(255, 128, 84, 0.2);">15+ min saved per meeting</div>
</div>
```

---

## Featured Tool Section — Deep Dive

**Location:** Lines ~128-200

This is the star section: a 3-column layout showing before/strategy/after for your main tool.

### Section Header

```html
<div class="section-label">[FEATURED_SECTION_LABEL]</div>
<h2 class="section-title">[FEATURED_TOOL_TITLE]</h2>
<p class="section-desc">[FEATURED_TOOL_LONG_DESC]</p>
```

**Examples:**

Joshua's:
```html
<div class="section-label">The Differentiator</div>
<h2 class="section-title">Negotiation Guidance (Black Swan Method)</h2>
<p class="section-desc">Difficult customer conversations are high-stakes and time-pressured. This skill brings Chris Voss's Black Swan methodology to every interaction, consistently, without requiring you to be a trained negotiator. Deploy it for renewals, escalations, scope disputes, or any conversation where you need tactical empathy and calibrated responses.</p>
```

### Column 1: Before/Inbound

```html
<div class="feature-panel">
  <div class="feature-panel-header">
    <div class="feature-step-dot">1</div>
    Inbound Message
  </div>
  <div class="feature-panel-body">
    <div class="feature-email">
      <div class="sender">[CUSTOMER_NAME] · [DATE]</div>
      [FEATURE_PANEL_1_CONTENT]
    </div>
  </div>
</div>
```

**Example (Joshua's negotiation before):**
```html
<div class="sender">Marcus Chen, VP Engineering · May 20</div>
We need to talk about renewal. Your team has been responsive, but we're seeing [feature X] behave inconsistently. Before we commit to another year, this needs to be resolved. We've also had conversations with [Competitor] and they're saying they can deliver this more reliably. We need to understand how you plan to address this, or we'll have to explore alternatives.
```

### Column 2: Strategy

```html
<div class="feature-panel">
  <div class="feature-panel-header">
    <div class="feature-step-dot">2</div>
    Strategy
  </div>
  <div class="feature-panel-body">
    <div style="font-size: 0.85rem; color: rgba(255,255,255,0.7); line-height: 1.7;">
      [FEATURE_PANEL_2_CONTENT]
    </div>
    <div style="margin-top: 1rem;">
      <span class="tactic-tag">[TACTIC_1]</span>
      <span class="tactic-tag">[TACTIC_2]</span>
      <span class="tactic-tag">[TACTIC_3]</span>
    </div>
  </div>
</div>
```

**Example (Joshua's strategy):**
```html
1. Accusation Audit: Surface all the negatives they're thinking (feature inconsistency, competitive evaluation)
2. Label: Validate the frustration without over-apologizing
3. Calibrated Question: Ask what success looks like for them, not what we can do
4. Tactical Empathy: Demonstrate understanding of their business constraints
5. Summary: Restate the full picture until they say "that's right"
```

**Tactics to include:**
- `Tactical Empathy`
- `Accusation Audit`
- `Label`
- `Mirror`
- `Calibrated Question`
- `No-Oriented Question`
- `Dynamic Silence`
- `Summary`
(Or whatever methodology applies to your workflow)

### Column 3: After/Response

```html
<div class="feature-panel">
  <div class="feature-panel-header">
    <div class="feature-step-dot">3</div>
    Response Draft
  </div>
  <div class="feature-panel-body">
    <div class="feature-email">
      <div class="sender">You · Ready to send</div>
      [FEATURE_PANEL_3_CONTENT]
    </div>
  </div>
</div>
```

**Example (Joshua's response):**
```html
Marcus — I want to make sure I understand the full picture before we talk through what's next. You're concerned about the inconsistency in [Feature X], and you're evaluating [Competitor] because they're claiming better reliability. That would put you in a position where you've committed internal resources to our roadmap but you're not confident in the delivery. Is that right?

[... continues with validated understanding, then problem-solving approach ...]
```

### Time Saved Metrics

```html
<div class="time-saved">
  <div class="time-item">
    <div class="time-number">[TIME_SAVED_1_NUMBER]</div>
    <div class="time-label">[TIME_SAVED_1_LABEL]</div>
  </div>
  <div class="time-divider"></div>
  <div class="time-item">
    <div class="time-number">[TIME_SAVED_2_NUMBER]</div>
    <div class="time-label">[TIME_SAVED_2_LABEL]</div>
  </div>
  <div class="time-divider"></div>
  <div class="time-item">
    <div class="time-number">[TIME_SAVED_3_NUMBER]</div>
    <div class="time-label">[TIME_SAVED_3_LABEL]</div>
  </div>
</div>
```

**Example:**
```html
<div class="time-number">15+</div>
<div class="time-label">minutes saved per difficult conversation</div>

<div class="time-number">30</div>
<div class="time-label">Enterprise accounts × 20% more proactive time</div>

<div class="time-number">100%</div>
<div class="time-label">back to relationship building vs. firefighting</div>
```

---

## Other Tools Section (3 tools)

**Location:** Lines ~221-310

Each tool follows a pattern: icon, name, description, before/after flow, impact.

```html
<div class="tool-detail-card fade-up">
  <div class="tool-detail-icon">[TOOL_A_ICON]</div>
  <h3>[TOOL_A_NAME]</h3>
  <p>[TOOL_A_DESC]</p>
  <div class="flow-diagram">
    <div class="flow-step">[FLOW_A_1]</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step">[FLOW_A_2]</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step">[FLOW_A_3]</div>
  </div>
  <div style="margin-top: 1.25rem;">
    <span class="impact-pill">[IMPACT_A]</span>
  </div>
</div>
```

**Example (Usage Reporting):**
```html
<div class="tool-detail-icon">📊</div>
<h3>Usage Reporting Automation</h3>
<p>Monthly data pulls for usage reporting and QBR prep used to eat 4 hours at month-end and 3 hours before every quarterly review. A colleague and I collaborated to turn that painstaking, manual process into a mostly automated output. That time goes back to customer conversations.</p>

<div class="flow-diagram">
  <div class="flow-step">Raw usage data</div>
  <div class="flow-arrow">→</div>
  <div class="flow-step">Automated pull</div>
  <div class="flow-arrow">→</div>
  <div class="flow-step">Formatted report</div>
  <div class="flow-arrow">→</div>
  <div class="flow-step">QBR-ready</div>
</div>

<span class="impact-pill">7+ hours saved monthly</span>
```

**Repeat this pattern 3 times** (TOOL_A, TOOL_B, TOOL_C).

### Toolchain Section

The 4th card in this section lists the technologies you used:

```html
<div class="tool-detail-card fade-up">
  <div class="tool-detail-icon">🛠️</div>
  <h3>The Toolchain</h3>
  <p>[TOOLCHAIN_DESC]</p>
  <div style="margin-top: 1rem; display: flex; flex-wrap: wrap; gap: 0.5rem;">
    <span style="background: var(--cream); border: 1px solid var(--warm-gray); border-radius: 6px; padding: 0.3rem 0.7rem; font-size: 0.8rem; color: var(--text-primary);">[TOOL_TECH_1]</span>
    <span style="background: var(--cream); border: 1px solid var(--warm-gray); border-radius: 6px; padding: 0.3rem 0.7rem; font-size: 0.8rem; color: var(--text-primary);">[TOOL_TECH_2]</span>
    <span style="background: var(--cream); border: 1px solid var(--warm-gray); border-radius: 6px; padding: 0.3rem 0.7rem; font-size: 0.8rem; color: var(--text-primary);">[TOOL_TECH_3]</span>
    <span style="background: var(--cream); border: 1px solid var(--warm-gray); border-radius: 6px; padding: 0.3rem 0.7rem; font-size: 0.8rem; color: var(--text-primary);">[TOOL_TECH_4]</span>
  </div>
</div>
```

**Example:**
```html
<p>None of this required a formal development background. It required curiosity, a clear sense of what problems needed solving, and a willingness to iterate until the tool actually worked the way the workflow needed it to.</p>

<span>Claude Opus 4.x</span>
<span>OpenCode</span>
<span>Windsurf / Cascade</span>
<span>Cloudflare Workers</span>
```

---

## Adoption / Organizational Impact Section

**Location:** Lines ~316-343

Three cards showing proof that your tools are being used:

```html
<div class="adoption-card fade-up">
  <div class="quote">[ADOPTION_QUOTE_1]</div>
  <div class="attribution">[ADOPTION_ATTRIBUTION_1]</div>
</div>
```

**Examples:**

Card 1:
```html
<div class="quote">"The negotiation skill changed how our team approaches difficult renewal conversations."</div>
<div class="attribution">Distributed by the Sr. Director of Global Sales Programs to the Cloudflare sales organization</div>
```

Card 2:
```html
<div class="quote">"Featured in multiple CS team meetings and highlighted in the weekly CS org newsletter with How-To guides."</div>
<div class="attribution">Cloudflare Global CS Organization</div>
```

Card 3:
```html
<div class="quote">"Invited to join the GCS AI Task Force to help advance AI adoption across the global CS team."</div>
<div class="attribution">Cloudflare Global Customer Success Leadership</div>
```

**Tips:**
- Use real testimonials or documented adoption evidence
- Be specific about who's using it and where
- Include organizational reach (sales org, CS team, internal task force, etc.)

---

## Call-to-Action Section

**Location:** Lines ~346-353

```html
<div class="section-label">[CTA_LABEL]</div>
<h2 class="section-title">[CTA_TITLE]</h2>
<p class="section-desc">[CTA_DESC]</p>
<div class="cta-links">
  <a href="[LINKEDIN_URL]" class="cta-primary" target="_blank">Connect on LinkedIn</a>
  <button class="cta-primary" id="emailBtn" onclick="handleEmail()">Send me an email</button>
</div>
```

**Examples:**

Joshua's:
```html
<div class="section-label">Let's Connect</div>
<h2 class="section-title">Want to talk about what I can build for your CS team?</h2>
<p class="section-desc">I'm actively exploring Senior CSM roles in industries such as Cybersecurity, SaaS, and Cloud Infrastructure. If you're building a team that has real problems to solve and you want someone who thinks critically, looks for efficiencies, and is a builder — let's talk.</p>

<a href="https://linkedin.com/in/joshualyons" class="cta-primary" target="_blank">Connect on LinkedIn</a>
```

**Tips:**
- Be specific about role titles you're targeting
- Mention industries
- Lead with what you're looking for, not what you're avoiding

---

## Footer

**Location:** Lines ~355-359

```html
<footer>
  <p>[YOUR_NAME]</p>
  <span class="pipe">|</span>
  <p><a href="[LINKEDIN_URL]" target="_blank">[LINKEDIN_HANDLE]</a></p>
</footer>
```

**Example:**
```html
<footer>
  <p>Joshua J. Lyons</p>
  <span class="pipe">|</span>
  <p><a href="https://linkedin.com/in/joshualyons" target="_blank">linkedin.com/in/joshualyons</a></p>
</footer>
```

---

## Email Obfuscation (JavaScript)

**Location:** Lines ~366-372

This uses character codes to hide your email from bots. Convert your email to char codes:

**In your browser console:**
```javascript
Array.from("yourname@gmail.com").map(c => c.charCodeAt(0))
// Output: [121, 111, 117, 114, 110, 97, 109, 101, 64, 103, 109, 97, 105, 108, 46, 99, 111, 109]
```

**Split the codes at the `@` symbol:**
- Before `@` (username): first array
- After `@` (domain): second array

```javascript
function handleEmail() {
  const p = [121, 111, 117, 114, 110, 97, 109, 101]; // "yourname"
  const d = [103, 109, 97, 105, 108, 46, 99, 111, 109]; // "gmail.com"
  const addr = p.map(c => String.fromCharCode(c)).join('') + '@' + d.map(c => String.fromCharCode(c)).join('');
  window.location.href = 'mailto:' + addr;
}
```

---

## Optional: Customizing Colors

**Location:** Lines 13-25 (the `:root` CSS variables)

If you want to change the color scheme, edit these at the top:

```css
:root {
  --navy: #0D1B2A;        /* Dark background color */
  --orange: #F4622A;      /* Accent color (buttons, links) */
  --cream: #FAF8F5;       /* Light background */
  --warm-gray: #E8E4DC;   /* Border color */
  --text-primary: #0D1B2A; /* Main text */
}
```

**Popular alternatives:**
- Navy → `#1A3A4A` (teal-navy)
- Orange → `#FF6B35` (deeper orange)
- Orange → `#4A90E2` (blue)

Change the hex codes and the entire site updates automatically.

---

## Checklist Before Deploying

- [ ] Replaced all `[PLACEHOLDER]` fields
- [ ] Updated email char codes
- [ ] Updated LinkedIn URL (2 places: button + footer)
- [ ] Added 4 hero statistics
- [ ] Filled in featured tool (3 columns)
- [ ] Filled in 3 additional tools
- [ ] Added adoption/testimonial quotes
- [ ] Tested email button (should open mail client)
- [ ] Tested on mobile (Chrome DevTools)
- [ ] Deployed to Cloudflare Pages
- [ ] Verified live site loads correctly

---

**Ready to deploy?** See [README.md](./README.md) for Cloudflare Pages setup instructions.
