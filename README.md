# MedModr: Mediation & Moderation Analysis Tool

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-blue.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Platform](https://img.shields.io/badge/Platform-Web%20%7C%20Offline-brightgreen)](https://shinyhealthtools.github.io/medmodr/)
[![Version](https://img.shields.io/badge/Version-1.0.0-blue)](https://github.com/shinyhealthtools/medmodr)

**MedModr** is a free, open-source web application for advanced statistical analyses including simple mediation, serial mediation, moderation, and moderated mediation (conditional process analysis).

All computations run locally in your browser. **Your data never leaves your device** — a privacy-first alternative to commercial software.

> **🔌 Internet Requirement:** A connection is needed only during the **first launch** (online or local `index.html`) to load dependencies. After that, MedModr works **completely offline**.

## 🔗 Launch & Documentation

| Resource | Link |
| :--- | :--- |
| **Primary Website** | [https://shinyhealthtools.github.io/medmodr/](https://shinyhealthtools.github.io/medmodr/) |
| **Mirror** | [https://medmodr.vercel.app/](https://medmodr.vercel.app/) |
| **Offline Use** | Download `index.html` from this repo — first load requires internet, then works offline |
| **Full Documentation** | [https://shinyopensource.github.io/medmodr-documentation/](https://shinyopensource.github.io/medmodr-documentation/) (guides, formulas, video tutorials, examples) |

## ✨ Features

| Feature | Description |
| :--- | :--- |
| **Simple Mediation** | X → M → Y with path coefficients (b and β), Sobel test, bootstrap CIs, interactive path diagram |
| **Serial Mediation** | X → M1 → M2 → Y with specific and total indirect effects, bootstrap CIs |
| **Moderation** | X × W → Y with simple slopes at ±1 SD and mean, annotated plot |
| **Moderated Mediation** | Conditional indirect effects + Index of Moderated Mediation (IMM) with bootstrap CIs |
| **Bootstrap** | 1,000–10,000 resamples with percentile confidence intervals |
| **Interactive Diagrams** | Toggle unstandardized/standardized coefficients, p-values, color schemes |
| **Simple Slopes Plot** | Annotated with b and p-values; toggle legend; export high-res PNG |
| **APA Reporting** | APA-formatted summaries, copy-to-clipboard, Microsoft Word export |
| **Privacy** | 100% local processing — data never leaves your device |

## 📊 Analysis Types

| Analysis | Path |
| :--- | :--- |
| Simple Mediation | X → M → Y |
| Serial Mediation | X → M1 → M2 → Y |
| Moderation | X × W → Y |
| Moderated Mediation | Conditional indirect effect of X on Y via M, moderated by W |

## 🚀 Quick Start

### Online
1. Go to [https://shinyhealthtools.github.io/medmodr/](https://shinyhealthtools.github.io/medmodr/)
2. Select analysis type → Enter variables → Paste data (one value per line, no headers)
3. Add covariates (optional: first row = names, subsequent rows = values)
4. Set confidence level (90%/95%/99%) and bootstrap samples (1000–10,000)
5. Click **"Run Analysis"**

### Offline / Local
1. Download `index.html` from this repository
2. Open it in a browser **while online** (first time only — loads dependencies)
3. Thereafter, works offline indefinitely

## 📂 Data Format

**All inputs:** One numeric value per line. **No headers.**

| Variable | Example Input |
| :--- | :--- |
| X (Stress) | `2.3` `4.1` `3.8` `5.0` |
| M (Coping) | `3.1` `2.5` `4.2` `3.9` |
| Y (Wellbeing) | `5.2` `4.8` `4.1` `3.5` |

**Covariates:**
- Row 1: Variable names (space/tab separated) → `age education`
- Rows 2+: Values in same order → `25 16`

**Important Notes:**
- Binary/categorical variables must be manually dummy-coded (0/1) before pasting
- No missing data — use listwise deletion before analysis

## 📈 Output

| Output Type | Details |
| :--- | :--- |
| **Descriptives** | N, mean, SD, min, max for all variables |
| **Path Diagrams** | Interactive SVG — toggle b/β, p-values, B&W mode, dotted direct path |
| **Regression Tables** | b, SE, t, p, 95% CI, β, R, R², Adj. R², F-test |
| **Simple Slopes Plot** | At -1 SD, mean, +1 SD of moderator |
| **APA Summary** | Narrative results ready for manuscripts |
| **Export** | Copy to clipboard or download as `.doc` (Word) |

## 🛠️ Technology

- **Language:** Vanilla JavaScript (ES6+)
- **Algebra:** Custom OLS regression matrix implementation
- **Bootstrap:** Percentile CI with up to 10,000 resamples
- **Visuals:** SVG (path diagrams) + Canvas (slopes plots)
- **Dependencies:** Chart.js, Font Awesome, Google Fonts (loaded once at first launch)
- **Offline:** Fully functional after initial load

## 📄 License (MIT)

Free, open-source under the MIT License. You may use, modify, distribute, and host MedModr freely — even for commercial purposes. The only restrictions: keep the copyright notice and don't claim you wrote the original software.

[Full license terms](https://github.com/shinyhealthtools/medmodr/blob/main/LICENSE)

## 🐛 Bug Reports & Support

| Method | Link / Contact |
| :--- | :--- |
| **GitHub Issues (Recommended)** | [https://github.com/shinyhealthtools/medmodr/issues](https://github.com/shinyhealthtools/medmodr/issues) |
| **Email** | [mudassiribrahim30@gmail.com](mailto:mudassiribrahim30@gmail.com) |

**Please include:** Problem description, steps to reproduce, browser/version, screenshot/error message (if applicable).

> 📚 Check the [documentation](https://shinyopensource.github.io/medmodr-documentation/) before reporting — your question may already be answered.

## 🤝 Contributing

Contributions welcome: bug fixes, new features, documentation, translations, performance optimizations, testing.

**Process:**
1. Fork the repo: `https://github.com/shinyhealthtools/medmodr`
2. Clone your fork: `git clone https://github.com/YOUR_USERNAME/medmodr.git`
3. Create a branch: `git checkout -b feature/your-feature-name`
4. Make changes → test in browser
5. Commit: `git commit -m "Add: description"`
6. Push: `git push origin feature/your-feature-name`
7. Open a Pull Request to the `main` branch

---

**MedModr** — Transparent, private, professional statistical analysis.
