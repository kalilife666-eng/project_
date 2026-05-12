# project_phoenix (v1.0)

**Multi-Platform Canadian Charter Breach Analysis with CanLII, AI Verification & Legal Dictionary**

project_phoenix is a comprehensive legal analysis suite designed for both **Android** and **Desktop** environments. It leverages a shared Python-based analysis engine to detect potential Canadian Charter of Rights and Freedoms breaches, providing legal professionals with a powerful aid for case review.

`Human Rights Guard` has been separated into its own standalone project at `/home/s/human_rights_guard`. `project_phoenix` remains focused on Charter and criminal-procedure analysis.

---

## 📱 Platform Capabilities

### 📱 Android Application
- **Modern UI:** Built with Jetpack Compose for a native Android experience.
- **Embedded Engine:** Runs the core Python analysis engine locally via Chaquopy.
- **On-the-go Analysis:** Perform legal audits directly from your mobile device.

### 💻 Desktop Application
- **Feature-Rich GUI:** Powered by Tkinter for a comprehensive analysis environment.
- **Multi-Tab Interface:** Detailed views for document analysis, dictionary lookup, and AI Q&A.
- **Report Generation:** Export professional HTML and text reports.

---

## Features (Shared Engine)

### ⚖️ Charter Breach Analysis
- Automated detection of potential **Canadian Charter of Rights and Freedoms** breaches.
- Covers Sections 2(a)–15(1) with keyword analysis, breach indicators, and legal test frameworks.
- Confidence scoring (HIGH / MEDIUM / LOW) for each potential breach.

### 📚 Cross-Reference Integration
- **CanLII** — Search Canadian case law with API integration.
- **Criminal Law Notebook** — Topic browser with direct links for Charter analysis.

### 🤖 AI Verification (OpenAI GPT-4)
- AI-powered verification of Charter breach analysis accuracy.
- Term verification, disambiguation, and executive summary generation.

### 📖 Legal Dictionary
- **50+ authoritative Canadian legal definitions** (Criminal Code, SCC jurisprudence).
- Flags misuses, Americanisms, and inconsistent terminology.

### 🚫 Deflection & Ambiguity Detection
- Identifies vague quantifiers, hedging, passive obfuscation, and weasel words.
- Provides severity ratings and specific suggestions.

---

## Installation & Running

### 💻 Desktop
1. **Setup:**
   ```bash
   pip install -r requirements.txt
   ```
2. **Launch:**
   ```bash
   python run.py
   ```

### 📱 Android
1. **Build:** Open the `android/` directory in Android Studio.
2. **Deploy:** Use `./gradlew assembleRelease` to generate artifacts or deploy directly to a device.
3. **Artifacts:** Pre-built `project_phoenix-release.apk` is available in the root directory.

---

## API Configuration

---

## API Configuration

### CanLII (Free — Recommended)
1. Register at https://api.canlii.org/
2. Get your API key
3. In the app: **Settings → API Keys → CanLII API Key**

*Without a CanLII key, the app generates direct search URLs you can click.*

### OpenAI (For AI Verification)
1. Get an API key at https://platform.openai.com/
2. Set env variable: `export OPENAI_API_KEY="sk-..."`
3. Or enter via: **Settings → API Keys → OpenAI API Key**

*The app works fully without AI — AI adds verification and enhanced analysis.*

---

## Architecture

```
project_phoenix/
├── main.py                 # Full GUI application (tkinter)
├── run.py                  # Startup script
├── config.py               # Charter sections, Oakes test, settings
├── document_processor.py   # PDF/DOCX/TXT loader & citation finder
├── charter_analyzer.py     # Charter breach analysis engine
├── canlii_client.py        # CanLII API & Criminal Law Notebook client
├── legal_dictionary.py     # Canadian legal dictionary & deflection patterns
├── ai_integration.py       # OpenAI GPT-4 verification module
├── report_generator.py     # HTML & text report generation
├── requirements.txt        # Python dependencies
└── README.md               # This file
```

---

## Charter Sections Analyzed

| Section | Right |
|---------|-------|
| 2(a) | Freedom of Conscience and Religion |
| 2(b) | Freedom of Expression |
| 2(c) | Freedom of Peaceful Assembly |
| 2(d) | Freedom of Association |
| 7 | Life, Liberty and Security of the Person |
| 8 | Unreasonable Search and Seizure |
| 9 | Arbitrary Detention or Imprisonment |
| 10(a) | Right to be Informed of Offence |
| 10(b) | Right to Retain and Instruct Counsel |
| 11(a) | Right to Trial Within Reasonable Time |
| 11(b) | Presumption of Innocence |
| 11(c) | Right Not to Be Compelled as Witness |
| 11(d) | Independent and Impartial Tribunal |
| 12 | Cruel and Unusual Treatment/Punishment |
| 13 | Self-Incrimination |
| 14 | Right to an Interpreter |
| 15(1) | Equality Rights |
| s.1 | Oakes Test (Justification) |

---

## Disclaimer

⚠️ **This tool does not constitute legal advice.** It is an analytical aid only. All findings, breach analyses, and AI-generated content must be reviewed by a qualified Canadian legal professional. Automated analysis cannot replace the exercise of legal judgment.

## Distribution Notice

Developer contact: **kalilife666@gmail.com**

Publisher-provided access policy:
- Open source software available for free download for all Canadians without a law license.
- This software is intended to remain available for free download permanently.
- Contributions to the developers and their descendants are welcome via e-Transfer to **kalilife666@gmail.com**.
- Any user with a law license requires a paid subscription of **CAD $300/month**.

---

## License
MIT
