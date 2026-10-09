# Private deployment

## Streamlit Community Cloud

1. Publish this project to a private GitHub repository.
2. Sign in to Streamlit Community Cloud with the GitHub account that owns the repository.
3. Create an app using branch `main` and main file `app.py`.
4. Add these values in the app's Secrets settings:

```toml
OPENAI_API_KEY = "your-key"
OPENAI_MODEL = "gpt-4.1-mini"
```

5. Restrict app access to approved viewers using the sharing controls available for your account.
6. Test access in a private browser window before uploading sensitive business material.

## Data handling

- Do not commit company profiles, tender documents, results or secrets.
- Use the minimum company information required for matching.
- Uploaded document text may be sent to the configured AI provider.
- Review provider data controls and portal terms before production use.
- This MVP does not include persistent storage, tenant isolation, OCR, audit logging, scheduled tender discovery or submission automation.
