# 🎨 HTML Quick-Styler

> **AI-Powered HTML Page Generator with IBM Granite 3.3 2B Instruct**

[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)](https://python.org)
[![Gradio](https://img.shields.io/badge/Gradio-Latest-orange?style=for-the-badge&logo=gradio)](https://gradio.app)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-IBM%20Granite-yellow?style=for-the-badge&logo=huggingface)](https://huggingface.co/ibm-granite/granite-3.3-2b-instruct)
[![Colab](https://img.shields.io/badge/Google%20Colab-Ready-green?style=for-the-badge&logo=googlecolab)](https://colab.research.google.com)
[![NM](https://img.shields.io/badge/Naan%20Mudhalvan-SmartBridge-red?style=for-the-badge)](https://naanmudhalvan.tn.gov.in)

---

## 📌 Project Description

**HTML Quick-Styler** is an intelligent web page generation platform that leverages **IBM's Granite 3.3 2B Instruct** model to provide comprehensive HTML/CSS page creation with professional styling and responsive design.

The platform addresses the challenge of rapid web development by delivering:
- 🤖 AI-powered HTML generation from plain-English descriptions
- 🔍 Automatic section detection using keyword NLP
- 🎨 Modern CSS styling with animations and transitions
- 🌈 8 curated color palette schemes
- 📱 Production-ready responsive code output

> Built as part of the **Naan Mudhalvan Programme** — SmartBridge / Skill Wallet, Academic Year 2024–2025.

---

## ✨ Key Features

### 🤖 1. AI HTML Generation
- Powered by **IBM Granite 3.3 2B Instruct** via Hugging Face Transformers
- Generates complete, self-contained HTML + CSS from a single description
- Supports 8 section types: Hero, Features, About, Portfolio, Testimonials, Pricing, Contact, Footer
- **Smart section detection** — automatically detects which sections to include using keyword NLP
- Output includes semantic HTML5, SEO meta tags, Open Graph, and Twitter Card support

### 🌈 2. Eight Color Palettes

| Palette | Primary | Style |
|---------|---------|-------|
| `modern` | `#667eea` | Dark purple-blue minimal |
| `vibrant` | `#ff6b6b` | Dark red-orange energetic |
| `ocean` | `#0ea5e9` | Dark blue-cyan calm |
| `forest` | `#22c55e` | Dark green earthy |
| `sunset` | `#f97316` | Dark orange warm |
| `luxury` | `#eab308` | Dark gold premium |
| `creative` | `#9b59b6` | Dark purple artistic |
| `minimal` | `#2c3e50` | Dark grey-blue corporate |

Each palette provides **8 CSS custom properties** injected into `:root` for consistent theming across all generated sections.

### 📱 3. Responsive Design
- **Mobile-first CSS** with media queries for tablet (768px) and phone (480px)
- CSS Grid and Flexbox layouts that adapt to all screen sizes
- Sticky navigation bar with backdrop blur effect
- Smooth scroll behaviour and CSS animations
- Production-ready code that works in any modern browser

### 🖥️ 4. Interactive Gradio Interface — 5 Tabs

| Tab | Name | Description |
|-----|------|-------------|
| ✨ Tab 1 | Generate Page | Enter title + description → AI generates full HTML |
| 👁️ Tab 2 | Live Preview | Renders generated HTML as a live webpage |
| 🌈 Tab 3 | Color Palettes | Browse all 8 palettes with hex color values |
| 📄 Tab 4 | Templates | 3 ready-made templates (Portfolio, SaaS, Corporate) |
| 📖 Tab 5 | Guide | Usage guide with keyword reference tables |

---

## 🏗️ System Architecture

```
User Input (Title + Description + Color Style)
           │
           ▼
┌─────────────────────────────┐
│   Gradio UI (5 Tabs)        │  ← Presentation Layer
└─────────────┬───────────────┘
              │
              ▼
┌─────────────────────────────────────────────┐
│         Application Logic Layer             │
│  ┌─────────────┐  ┌──────────────────────┐  │
│  │  Section    │  │  ColorPalette        │  │
│  │  Detection  │  │  Generator (8 styles)│  │
│  │  (Keyword   │  │                      │  │
│  │   NLP)      │  │                      │  │
│  └──────┬──────┘  └──────────┬───────────┘  │
│         └─────────┬──────────┘              │
│                   ▼                         │
│         HTMLGenerationEngine                │
└───────────────────┬─────────────────────────┘
                    │
                    ▼
┌─────────────────────────────┐
│  IBM Granite 3.3 2B Instruct│  ← AI Generation Layer
│  (Hugging Face Transformers)│
└─────────────────────────────┘
                    │
                    ▼
     Production-Ready HTML + CSS Output
```

---

## 🚀 How to Run on Google Colab

### Step 1 — Open Google Colab
```
https://colab.research.google.com
```
Click **`+ New notebook`**

### Step 2 — Enable GPU Runtime ⚡
```
Runtime → Change runtime type → T4 GPU → Save
```

### Step 3 — Install Dependencies
```python
!pip install -q gradio transformers accelerate torch
```

### Step 4 — Upload or Paste the Script
Upload `html_quick_styler_colab.py` to Colab, or paste the full script into a code cell.

### Step 5 — Run the Application
```python
!python html_quick_styler_colab.py
```
Or if pasted directly, run the cell. You will see:
```
✅ Model ready on device: cuda
Running on public URL: https://xxxxxxxx.gradio.live
```

### Step 6 — Open the Interface
Click the **public Gradio URL** — it works on any device with a browser!

### Step 7 — Generate Your First Page
1. Go to **Tab 1 — Generate Page**
2. Enter a **Page Title** (e.g. `My Portfolio`)
3. Enter a **Description** (e.g. `hero section, features, about, contact form, footer`)
4. Select a **Color Style** from the dropdown
5. Click **✨ Generate HTML**
6. Switch to **Tab 2 — Live Preview** → click **▶ Load Preview**

---

## 💻 Local Installation (Optional)

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/html-quick-styler.git
cd html-quick-styler

# Create virtual environment
python -m venv .venv
.venv\Scripts\activate          # Windows
# source .venv/bin/activate     # Mac/Linux

# Install dependencies
python -m pip install gradio transformers accelerate torch

# Run
python html_quick_styler_colab.py
```
Open `http://127.0.0.1:7860` in your browser.

---

## 📁 Project Structure

```
html-quick-styler/
│
├── html_quick_styler_colab.py   # Main application script
├── README.md                    # This file
├── requirements.txt             # Python dependencies
│
└── docs/
    ├── NM_Project_Report.docx   # Full project report
    └── screenshots/             # Output screenshots
```

### requirements.txt
```
gradio
transformers>=4.40.0
torch>=2.0.0
accelerate
```

---

## 🧪 Test Cases

| Test Case | Input Title | Color Style | Sections | Result |
|-----------|------------|-------------|----------|--------|
| TC-01 | Modern Portfolio Website | modern | Hero, Features, About, Portfolio, Testimonials, Contact, Footer | ✅ Pass |
| TC-02 | TechFlow - AI Solutions | vibrant | Hero, Features, Pricing, Testimonials, Contact, Footer | ✅ Pass |
| TC-03 | BuildCorp Solutions | minimal | Hero, About, Services, Contact, Footer | ✅ Pass |
| TC-04 | Color Palette Exploration | All 8 | N/A | ✅ Pass |

---

## 👥 Team Members

| Name | Roll Number | Contribution |
|------|------------|--------------|
| R.Ponkarthick |  Reg. No. 23082261802111008 | Model Integration & AI Prompt Engineering |
| S.Sarankumar |  Reg. No. 23082261802111013 | ColorPaletteGenerator & CSS Engine |
| S.Ajay |  Reg. No. 23082261802111001 | HTMLPageBuilder & Section Templates |
| C.Ramasubbramanian |  Reg. No. 23082261802111011 | Gradio Interface & Deployment |

> 📍 **Institution:** Geetha Jeevan Arts and Science College  
> 📚 **Department:** B.Sc. Computer Science  
> 🎓 **Programme:** Naan Mudhalvan — SmartBridge / Skill Wallet  
> 📅 **Academic Year:** 2025–2026  

---

## 🛠️ Technologies Used

| Technology | Version | Purpose |
|-----------|---------|---------|
| Python | 3.8+ | Core application language |
| IBM Granite 3.3 2B | Latest | AI HTML generation |
| Hugging Face Transformers | 4.40+ | Model loading and inference |
| PyTorch | 2.0+ | Deep learning backend |
| Gradio | Latest | Interactive web interface |
| Google Colab | — | Cloud deployment platform |
| HTML5 / CSS3 | — | Generated page standards |

---

## 📸 Screenshots

| Generate Page | Live Preview | Color Palettes |
|--------------|-------------|----------------|
| *(Add screenshot)* | *(Add screenshot)* | *(Add screenshot)* |

---

## 🔮 Future Enhancements

- [ ] Custom color picker for user-defined palettes
- [ ] JavaScript interactivity generation
- [ ] Export to downloadable `.html` file button
- [ ] Integration with Tailwind CSS framework
- [ ] Image generation API for hero sections
- [ ] More section templates (FAQ, Blog, E-commerce)

---

## 📄 License

This project is developed for educational purposes under the **Naan Mudhalvan Programme** by the Tamil Nadu government in collaboration with SmartBridge Educational Services.

---

## 🙏 Acknowledgements

- **IBM Research** — for the Granite 3.3 2B Instruct open-source model
- **Hugging Face** — for the Transformers library and model hosting
- **Gradio / Hugging Face** — for the interactive UI framework
- **SmartBridge & Skill Wallet** — for project guidance and mentorship
- **Naan Mudhalvan Programme** — Tamil Nadu Government initiative

---

