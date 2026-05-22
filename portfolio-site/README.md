# AI Portfolio Site Template

A fork-friendly portfolio template for Customer Success professionals showcasing AI-powered workflows. Built with clean HTML/CSS, no build process required, and ready to deploy to Cloudflare Pages in minutes.

**Live example:** [Joshua J. Lyons AI Portfolio](https://jjl-ai-portfolio-site.gantoris22.workers.dev) ([GitHub repo](https://github.com/joshualyons22/jjl-ai-portfolio-site))

---

## What This Is

A single-file, static portfolio site designed to showcase:
- Your professional identity as a CS practitioner
- AI workflows you've built or use
- Quantified impact (time saved, adoption metrics)
- Easy path to contact you

**The pitch:** Most CSMs talk about using AI. This template lets you *show* it — with specific workflows, before/after comparisons, and proof that colleagues use what you've built.

---

## Quick Start

### 1. Fork or Clone This Repo

```bash
# Clone the repo
git clone https://github.com/joshualyons22/lyons-cs-jobsearch-skills.git
cd lyons-cs-jobsearch-skills/portfolio-site

# Or copy the index.html file and work locally
```

### 2. Customize the Template

Open `index.html` and replace all `[PLACEHOLDER]` fields with your content. See **[CUSTOMIZE.md](./CUSTOMIZE.md)** for line-by-line guidance.

Key fields to customize:
- `[YOUR_NAME]` — Your name (appears in nav, footer, and title)
- `[STAT_1_NUMBER]`, `[STAT_1_LABEL]` — 4 hero statistics
- `[FEATURED_TOOL_*]` — Your main AI workflow (3-column before/strategy/after layout)
- `[TOOL_A_*]`, `[TOOL_B_*]`, `[TOOL_C_*]` — 3 additional workflows
- `[ADOPTION_QUOTE_*]` — Proof of organizational impact
- Email character codes in the `handleEmail()` function

### 3. Convert Your Email Address

The email button uses character code obfuscation to avoid scraping. Convert your email:

```javascript
// In your browser console:
Array.from("yourname@gmail.com").map(c => c.charCodeAt(0))
// Output: [121, 111, 117, 114, 110, ...]

// Then replace these in the script:
const p = [121, 111, 117, 114, 110, 97, 109, 101]; // "yourname"
const d = [103, 109, 97, 105, 108, 46, 99, 111, 109]; // "gmail.com"
```

Or use an online [ASCII to char code converter](https://www.rapidtables.com/code/text/ascii-table.html).

### 4. Deploy to Cloudflare Pages

**Option A: GitHub Integration (Recommended)**

1. Push your customized `index.html` to your own GitHub repo
2. Go to https://dash.cloudflare.com → Workers & Pages
3. Click **Create application** → **Continue with GitHub**
4. Select your repo and click **Deploy**
5. Your site will be live at `[your-repo-name].pages.dev`

**Option B: Direct Upload**

1. Go to https://dash.cloudflare.com → Workers & Pages
2. Click **Create application** → **Upload your static files**
3. Upload `index.html`
4. Your site will be live immediately

---

## Customization Overview

The template has five main sections:

### Hero (Landing)
- Professional headline
- 4 key statistics
- 3 tool cards (2 regular + 1 featured)

### Featured Tool Section
A deep-dive into your main AI workflow with a 3-column layout:
1. **Before** — Inbound customer message or problem
2. **Strategy** — What you did (tactics, methodology, approach)
3. **After** — Ready-to-send response or outcome

Use this for your signature tool that demonstrates the most value.

### Other Tools
3 additional workflows with:
- Icon, title, description
- Before/after flow diagram
- Time/effort saved metric

### Organizational Impact
3 adoption/testimonial cards showing:
- Proof that colleagues use your tools
- Organizational distribution (sold to Sales org, featured in newsletter, etc.)
- Recognition or feedback

### Call-to-Action
Final section with LinkedIn button and email obfuscation.

---

## Design System

**Colors** (easy to customize in the `:root` CSS section):
- Navy: `#0D1B2A`
- Orange: `#F4622A`
- Cream: `#FAF8F5`

**Fonts**:
- Display: DM Serif Display
- Body: DM Sans
- (Both from Google Fonts; loaded automatically)

**Responsive**:
The template is mobile-responsive out of the box. Test on mobile before deploying.

---

## Deployment

### Cloudflare Pages (Free)

After pushing to GitHub or uploading files:

1. **Auto-deploy on git push** — Connect your GitHub repo in Cloudflare Pages settings
2. **Custom domain** — Point your domain to Cloudflare Pages (optional)
3. **Instant HTTPS** — Enabled automatically

Example live URL: `jjl-ai-portfolio-site.gantoris22.workers.dev`

### Other Platforms

This is a static HTML file — deploy it anywhere:
- **Vercel** — `vercel deploy index.html`
- **Netlify** — Drag-and-drop the file
- **GitHub Pages** — Push to a `gh-pages` branch
- **Your own server** — Copy the file and serve it

---

## Tips for Your Content

### Hero Statistics
Lead with quantified impact. Examples:
- `100% | Logo retention`
- `$4M | ARR protected in saves`
- `4 hrs | Saved monthly on reporting`
- `1hr/day | Time back to customers`

### Featured Tool
Pick your **highest-leverage AI workflow**. This should be:
- Something you use regularly
- Something colleagues also use
- Quantifiable (time saved, adoption metrics)
- Shows methodology (not just "I used AI")

### Adoption Proof
Include real evidence:
- Internal distribution ("Distributed by the Sr. Director of Global Sales Programs...")
- Newsletter/team features
- Task force invitations
- Testimonials from colleagues
- Adoption metrics

### Call-to-Action
Be specific about what you're looking for:
- Role title (Sr. CSM, Manager of CS)
- Industries (Cybersecurity, SaaS, Cloud)
- Why you're motivated

---

## Customization Checklist

- [ ] Replace all `[PLACEHOLDER]` fields with your content
- [ ] Update email character codes in the `handleEmail()` function
- [ ] Update LinkedIn URL (appears twice: LinkedIn button + footer)
- [ ] Update hero statistics and descriptions
- [ ] Fill in featured tool (before/strategy/after)
- [ ] Fill in 3 additional tools
- [ ] Add adoption quotes and attributions
- [ ] Update CTA copy and LinkedIn handle
- [ ] Test on mobile (use Chrome DevTools)
- [ ] Deploy to Cloudflare Pages
- [ ] Share in networking conversations and LinkedIn

---

## File Structure

```
portfolio-site/
├── index.html          # The complete site (single file)
├── README.md           # This file
├── CUSTOMIZE.md        # Detailed customization guide
└── examples/           # (Optional) Example before/after content
    └── negotiation-example.txt
```

---

## Troubleshooting

**Site doesn't load after deployment**
- Check that `index.html` is in the root of your Cloudflare Pages project
- Verify the Cloudflare deployment log for errors

**Email button doesn't work**
- Verify your character codes are correct
- Test in the browser console: `handleEmail()` should open your mail client

**Styling looks broken**
- Ensure Google Fonts are loading (check the `<link>` tags in the `<head>`)
- Clear browser cache and reload

**Mobile layout looks off**
- The template includes media queries for responsive design
- Test with Chrome DevTools device emulation

---

## Support

**Questions about customization?** See [CUSTOMIZE.md](./CUSTOMIZE.md) for line-by-line guidance.

**Want to contribute improvements?** Submit a pull request to the [main repo](https://github.com/joshualyons22/lyons-cs-jobsearch-skills).

**Found an issue?** Open an issue on GitHub.

---

## License

This template is shared freely for CS professionals. Fork it, customize it, and make it your own. Attribution appreciated but not required.

---

**Built by Joshua J. Lyons** | [LinkedIn](https://linkedin.com/in/joshualyons) | [Portfolio Example](https://jjl-ai-portfolio-site.gantoris22.workers.dev)
