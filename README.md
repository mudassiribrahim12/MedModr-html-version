# MedModr: Mediation & Moderation Analysis Tool

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-blue.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Platform](https://img.shields.io/badge/Platform-Web%20%7C%20Offline-brightgreen)](https://shinyhealthtools.github.io/medmodr/)
[![Version](https://img.shields.io/badge/Version-1.0.0-blue)](https://github.com/shinyhealthtools/medmodr)
[![GitHub Issues](https://img.shields.io/badge/Report-Bugs-red)](https://github.com/shinyhealthtools/medmodr/issues)

**MedModr** (Mediation & Moderation) is a free, open-source web application for conducting advanced statistical analyses including simple mediation, serial mediation, moderation, and moderated mediation (conditional process analysis).

All computations are performed locally in your browser. Your data never leaves your device, making it a privacy-focused alternative to commercial software.

> ⚡ **Internet Connection Requirement (One-Time Only):** You need an internet connection **only for the first time you open MedModr** – whether using the online links or the downloaded `index.html` file. This initial load fetches essential resources (CSS, fonts, libraries). After that, the app works **completely offline** with full functionality.

## 🔗 Launch MedModr & Documentation

You can start using MedModr immediately via any of these links:

- **Primary Website:** [https://shinyhealthtools.github.io/medmodr/](https://shinyhealthtools.github.io/medmodr/)
- **Mirror / Alternative:** [https://medmodr.vercel.app/](https://medmodr.vercel.app/)
- **Offline / Local Use:** Download the `index.html` file from this repository and open it in any modern web browser. **Note:** An internet connection is required for the first load to download dependencies. After that, the tool works completely offline.
- **📚 Full Documentation & Video Tutorials:** [https://shinyopensource.github.io/medmodr-documentation/](https://shinyopensource.github.io/medmodr-documentation/)

The documentation website includes detailed step-by-step guides, mathematical formulas, video tutorials, and examples for every analysis type.

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| **Simple Mediation** | X → M → Y with full path coefficients (b and β), Sobel test, bootstrap CIs, and an interactive path diagram. |
| **Serial Mediation** | X → M1 → M2 → Y with specific indirect paths, total indirect effects, and bootstrap CIs. |
| **Moderation** | X × W → Y with unstandardized/standardized coefficients, simple slopes at ±1 SD and mean, and an annotated plot. |
| **Moderated Mediation** | Conditional indirect effects and the index of moderated mediation (IMM) with bootstrap CIs. |
| **Bootstrap Resampling** | User-selectable resamples (1,000–10,000) for robust percentile confidence intervals. |
| **Interactive Diagrams** | Real-time path diagrams with toggleable unstandardized/standardized coefficients, p-values, and color schemes. |
| **Annotated Slopes Plot** | Simple slopes plot with b and p-value labels; toggle annotations, legend, and download high-resolution PNGs. |
| **Export & APA Reporting** | APA-formatted summaries, copy-to-clipboard functionality, and Microsoft Word document export. |
| **Complete Privacy** | All data processing occurs locally. You can disconnect from the internet after the page loads. |

## 📊 Analysis Types

### 1. Simple Mediation (X → M → Y)
Evaluates whether the effect of an independent variable (X) on an outcome (Y) is transmitted through a mediator (M).

### 2. Serial Mediation (X → M1 → M2 → Y)
Tests a causal chain where X influences Y through two sequential mediators.

### 3. Moderation (X × W → Y)
Examines whether the effect of X on Y depends on the level of a moderator variable (W). Includes simple slopes analysis at three levels of W.

### 4. Moderated Mediation (Conditional Process Analysis)
Tests whether an indirect effect (X → M → Y) is conditional on the value of a moderator (W).

## 🚀 How to Use

### Method 1: Online Access
1.  Navigate to [https://shinyhealthtools.github.io/medmodr/](https://shinyhealthtools.github.io/medmodr/) or [https://medmodr.vercel.app/](https://medmodr.vercel.app/).
2.  **Internet required for first load only.** After the page loads, you can disconnect from the internet and continue using the tool.
3.  Select your analysis type from the "Analysis" tab.
4.  Enter variable names and paste your data (one value per line, no headers).
5.  Optionally, add covariates (first row = variable names, subsequent rows = data).
6.  Choose your confidence level (90%, 95%, 99%) and number of bootstrap samples (1000, 5000, 10,000).
7.  Click **"Run Analysis"** to view results, including tables, diagrams, and APA summaries.

### Method 2: Offline / Local Use
1.  Download the `index.html` file from this repository.
2.  **First-time setup:** Open the downloaded file with any modern web browser (Chrome, Firefox, Edge, Safari) while **connected to the internet**. This allows the app to load all required dependencies (fonts, CSS, libraries).
3.  **After the first successful load,** you can disconnect from the internet. The tool will work completely offline, and you can even close and reopen the file without an internet connection (browser cache will serve the resources).
4.  The tool will function identically to the online version without requiring an internet connection for subsequent uses.

### Method 3: Learn with Documentation & Tutorials
- Visit the **official documentation**: [https://shinyopensource.github.io/medmodr-documentation/](https://shinyopensource.github.io/medmodr-documentation/)
- Watch **video tutorials** demonstrating each analysis step-by-step.
- Review **mathematical formulas** and methodological references.
- Explore **example datasets** and interpretation guides.

## 📂 Data Format Guide

All data input fields require one numeric value per line. **Do not include headers.**

### Example for Simple Mediation

| Variable Name | Input Format |
| :--- | :--- |
| **X (Stress)** | `2.3`<br>`4.1`<br>`3.8`<br>`5.0`<br>`...` |
| **M (Coping)** | `3.1`<br>`2.5`<br>`4.2`<br>`3.9`<br>`...` |
| **Y (Wellbeing)** | `5.2`<br>`4.8`<br>`4.1`<br>`3.5`<br>`...` |

### Covariates Format
- **Row 1:** Variable names separated by spaces or tabs (e.g., `age education`).
- **Rows 2+:** Data values in the same order as the headers (e.g., `25 16`).

### Important Notes on Data
- **Binary Variables (Dummy Coding):** MedModr does not automatically convert categorical variables (e.g., gender, treatment group) into dummy codes. All categorical predictors must be converted by the user into numeric 0/1 dummy variables before pasting data.
- **Missing Data:** Currently, MedModr requires complete data (listwise deletion). All variables must have equal N with no missing values. Pre-process your data before analysis.

## 📈 Output and Interpretation

For each analysis, MedModr provides:

1.  **Descriptive Statistics:** Table of N, mean, SD, min, and max for all variables.
2.  **Path Diagrams:** Interactive SVG diagrams. You can toggle:
    - Unstandardized (b) vs. Standardized (β) coefficients.
    - Display of p-values.
    - Black & white mode for publication.
    - Dotted style for the direct effect path.
3.  **Regression Tables:** For each model in the analysis, including:
    - Coefficients (b), SE, t, p, and 95% CI.
    - Standardized coefficients (β) in a separate column.
    - Model fit statistics (R, R², Adj. R², F-test).
4.  **Simple Slopes Plot:** For moderation and moderated mediation, an interactive plot at -1 SD, mean, and +1 SD of the moderator.
5.  **APA-Style Summary:** A narrative summary of the results.
6.  **Export Options:** Copy all results to clipboard or export to a `.doc` Word file.

## 🛠️ Technical Details

- **Language:** Vanilla JavaScript (ES6+)
- **Matrix Algebra:** Custom implementation for OLS regression
- **Bootstrap:** Up to 10,000 resamples with percentile CI
- **Visualization:** SVG for path diagrams, Canvas for simple slopes plots
- **Dependencies:** Chart.js (for future enhancements), Font Awesome, Google Fonts
- **Offline Capable:** Yes, works completely offline after initial page load

## 📄 License (MIT)

MedModr is open-source software released under the **MIT License**. You are free to use, modify, and distribute it, subject to the terms: [https://github.com/shinyhealthtools/medmodr/blob/main/LICENSE](https://github.com/shinyhealthtools/medmodr/blob/main/LICENSE)

### What This Means For You

| Action | Permitted? |
| :--- | :--- |
| ✅ Download and use MedModr for free | Yes |
| ✅ Use it for commercial purposes | Yes |
| ✅ Modify the source code | Yes |
| ✅ Create your own versions | Yes |
| ✅ Host MedModr on your own servers | Yes |
| ✅ Include it in research or teaching | Yes |
| ✅ Distribute copies | Yes |
| ⚠️ Remove the copyright notice | No |
| ⚠️ Claim you wrote the original software | No |
| ⚠️ Hold the developer liable for issues | No |

## 🐛 Reporting Bugs & Getting Support

If you encounter any issues while using MedModr, there are **two ways** to report them:

### Option 1: GitHub Issues (Recommended)
- **Open an issue:** [https://github.com/shinyhealthtools/medmodr/issues](https://github.com/shinyhealthtools/medmodr/issues)
- **Benefits:** Public tracking, community discussion, ability to attach screenshots/files, and direct integration with development.
- **Please include:**
  - Description of the problem
  - Steps to reproduce
  - Browser and version you're using
  - Screenshot or error message (if applicable)
  - Data sample (if possible without compromising privacy)

### Option 2: Direct Email
- **Email:** [mudassiribrahim30@gmail.com](mailto:mudassiribrahim30@gmail.com)
- **Best for:** Private issues, sensitive data concerns, or if you don't have a GitHub account.
- **Please include the same details as above.**

> 💡 **Before reporting:** Please check the [documentation website](https://shinyopensource.github.io/medmodr-documentation/) first. Your question may already be answered there!

## 🤝 Contributing to MedModr

MedModr is open source and **welcomes contributions** from the community! Whether you want to fix a bug, add a feature, improve documentation, or translate the interface, your help is appreciated.

### Ways You Can Contribute

| Contribution Type | Description |
| :--- | :--- |
| 🐛 **Bug Fixes** | Help identify and fix issues in the code. |
| ✨ **New Features** | Add new analysis types or visualization options. |
| 📖 **Documentation** | Improve the docs, add examples, or fix typos. |
| 🌐 **Translation** | Translate the interface to other languages. |
| ⚡ **Performance** | Optimize code for large datasets. |
| 🧪 **Testing** | Test the tool with different datasets and report issues. |

### How to Contribute (Fork & Pull Request)

Follow these steps to contribute code or documentation changes:

#### Step 1: Fork the Repository
- Go to: [https://github.com/shinyhealthtools/medmodr](https://github.com/shinyhealthtools/medmodr)
- Click the **"Fork"** button (top-right corner) to create a copy under your GitHub account.

#### Step 2: Clone Your Fork Locally
- Run: git clone https://github.com/YOUR_USERNAME/medmodr.git  
- Then: cd medmodr  

#### Step 3: Create a New Branch
- Run: git checkout -b feature/your-feature-name  
- Or for bug fixes: git checkout -b fix/issue-description  

#### Step 4: Make Your Changes
- Edit the index.html file or other relevant files.  
- Test your changes thoroughly in a browser.  

#### Step 5: Commit Your Changes
- Run: git add .  
- Then: git commit -m "Add: description of your change"  
- Use prefixes like Add:, Fix:, Docs:, Refactor: for clarity.  

#### Step 6: Push to Your Fork
- Run: git push origin feature/your-feature-name  

#### Step 7: Open a Pull Request
- Go to your fork on GitHub.  
- Click "Compare & pull request" button.  
- Write a clear description of your changes.  
- Submit the pull request to the main branch of the original repository.  
