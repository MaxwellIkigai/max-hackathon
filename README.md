# Max Hackathon - Bank Designer Live Demo

AI-powered bank app generator with live split-view preview. Built with the **bank-designer agent** — no backend connections required.

![Demo](https://img.shields.io/badge/Status-Live%20Demo-success)
![License](https://img.shields.io/badge/License-MIT-blue)

## 🎯 Features

- **Live Code Preview** — Watch code being typed line-by-line
- **Component Rendering** — App builds component-by-component in real-time
- **4 Bank Segments** — Wealth, Mass-Market, Neobank, Kenya Transaction
- **Design Tokens** — Consistent color, typography, spacing per segment
- **No Backend** — Pure frontend, runs entirely in the browser
- **Bank Designer Agent** — Powered by `.opencode/agent/bank-designer.md`

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/MaxwellIkigai/max-hackathon.git
cd max-hackathon/frontend

# Open in browser
open src/index.html

# Or use a dev server
python3 -m http.server 8000
# Then open http://localhost:8000/src/
```

## 🏗 Architecture

### Frontend Structure
```
frontend/
├── src/
│   ├── index.html    # Main app (split-view IDE)
│   └── style.css     # Ikigai Digital design system
```

### Design Segments

| Segment | Colors | Typography | Spacing | Use Case |
|---------|--------|------------|---------|----------|
| **Wealth** | Navy #1E3A5F + Gold #d4af37 | Playfair Display (serif) | Spacious (24-48px) | High-net-worth, investment-first |
| **Mass-Market** | Green #16a34a + Blue | Inter (sans-serif) | Efficient (12-24px) | Everyday banking, bills, airtime |
| **Neobank** | Purple #8b5cf6 + Pink #ec4899 | Inter (bold, geometric) | Medium (16-32px) | Digital-first, feed-based UI |
| **Kenya** | Green #16a34a + Orange #f97316 | Inter | Tight (12-20px) | Transaction-focused, M-Pesa, airtime |

## 🎨 How It Works

1. **Select a Preset** — Click a chip (Wealth, Mass-Market, Neobank, Kenya)
2. **Watch Generation** — 3-step progress: Analyze → Apply Tokens → Build
3. **Code Types Live** — HTML appears line-by-line in center panel (15ms/line)
4. **Preview Renders** — iPhone frame on right updates in real-time
5. **Copy & Export** — Click "Copy" to grab the full HTML

## 📱 Templates Included

### Wealth Bank
- Total Portfolio Value hero (€2.8M)
- Playfair Display serif for numbers
- Gold CTA: "Speak to Your Advisor"
- YTD Return +12.4%, Risk Score 6.2

### Mass-Market Bank
- KSh 42,850 balance
- Quick actions: Send Money, Buy Airtime, Pay Bills
- 3x3 services grid: Safaricom, Kenya Power, School Fees

### Neobank
- $12,450 balance with weekly gain
- Feed-based UI with avatar cards
- Cashback notifications, subscription tracking

### Kenya Transaction Bank
- KSh balance with M-Pesa integration
- Airtime: Safaricom + Airtel
- Promo banner: "Get 5% Back on All Bills!"
- Services: DStv, Kenya Power, Nairobi Water

## 🤖 Bank Designer Agent

Located in `.opencode/agent/bank-designer.md`

**What it does:**
- Reads PRD JSON files with embedded design briefs
- Applies segment-specific design tokens (color, typography, spacing)
- Generates token-driven HTML with `var(--token)` CSS
- Ensures consistent design language across all bank apps

**Modes:**
1. **Apply Tokens to PRD** — Add `designLanguage` object to PRD JSON
2. **Design Home Screen** — Generate HTML from PRD with design brief

## 🔧 Customization

### Add Your Own Bank Template

Edit `index.html` and add to `BANK_TEMPLATES`:

```javascript
BANK_TEMPLATES.mybank = {
  name: "My Custom Bank",
  tokens: {
    colorBrand: "#your-color",
    colorAccent: "#accent-color",
    fontDisplay: "'Your Font', serif",
    space: "16px 24px 32px"
  },
  html: `<!-- YOUR HTML HERE -->`
};
```

Then add a preset chip:
```html
<button class="chip" data-segment="mybank">My Custom Bank</button>
```

### Modify Design Tokens

Each template has a `tokens` object:
- `colorBrand` — Primary brand color
- `colorAccent` — Secondary/CTA color
- `fontDisplay` — Hero number font (wealth only)
- `fontBody` — Body text font
- `space` — Padding scale (CSS custom properties)

## 📦 No Backend Required

**All templates are embedded in `index.html`:**
- No API calls
- No database
- No environment variables
- Pure HTML/CSS/JS

This makes it perfect for:
- ✅ Hackathons (no deployment complexity)
- ✅ Demos (open file, it works)
- ✅ Prototyping (instant iteration)
- ✅ Offline use (no network needed)

## 🎬 Demo Video

*Coming soon — record screen capture of live typing + preview rendering*

## 📄 License

MIT License - see LICENSE file for details

## 🙏 Credits

- **Frontend Architecture** — Cloned from [t5-thunder-lynx](https://github.com/ikigai-digital/t5-thunder-lynx)
- **Bank Designer Agent** — Built for portfolio-wide design language consistency
- **Design System** — Ikigai Digital brand guidelines
- **Highlight.js** — Code syntax highlighting (Atom One Dark theme)

## 🔗 Links

- [Live Demo](https://maxwellikigai.github.io/max-hackathon) *(deploy to GitHub Pages)*
- [Ikigai Digital](https://www.ikigaidigital.io/)
- [Original Repo](https://github.com/ikigai-digital/t5-thunder-lynx)

---

**Built with ❤️ for Max's Hackathon**

*Watch code write itself, see apps come to life.*
