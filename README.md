# TenderMatch AI

A Streamlit MVP that compares a company profile with public tender pages and official tender PDFs. It produces a plain-language shortlist, key eligibility conditions, possible evidence gaps, source references, and downloadable JSON/CSV reports.

## Features

- Upload a company profile PDF
- Enter a public tender-detail URL
- Upload one or more tender PDFs
- Extract company capabilities and documented credentials
- Summarize scope, dates, EMD/ePBG, turnover, experience and mandatory documents
- Classify each item as Potential match, Needs review, or Likely unsuitable
- Export results as JSON and CSV
- Block local/private-network URLs to reduce server-side request risks

## Local setup

1. Install Python 3.10 or newer.
2. Open a terminal in this folder.
3. Create a virtual environment:

```bash
python -m venv .venv
```

4. Activate it.

Windows:

```powershell
.venv\Scripts\activate
```

macOS/Linux:

```bash
source .venv/bin/activate
```

5. Install packages:

```bash
pip install -r requirements.txt
```

6. Copy `.env.example` to `.env` and add your API key.
7. Start the app:

```bash
streamlit run app.py
```

## GitHub Desktop

1. Extract the ZIP.
2. Open GitHub Desktop.
3. Choose **File > Add Local Repository** and select the extracted `TenderMatch-AI` folder.
4. If prompted, create a repository in that folder.
5. Commit all included files.
6. Choose **Publish repository** and keep it private if the source is not intended for public use.

Never add `.env`, API keys, company PDFs, tender PDFs or generated result files. The provided `.gitignore` excludes them.

## Important limitations

- This is decision support, not legal or eligibility advice.
- It does not bypass login, CAPTCHA or portal restrictions.
- JavaScript-heavy portals may not expose content to the app. Upload the official tender PDF instead.
- Scanned PDFs need OCR, which is not included in this MVP.
- Always verify the latest official tender, corrigenda, deadline, EMD/ePBG and submission instructions.
- Uploaded text is sent to the configured AI provider for analysis.
