# AppHub ZIP deployment

1. Create a fine-grained personal access token limited to this repository.
2. Grant **Contents: Read and write** only.
3. Open AppHub, enter the token, app name and ZIP archive, then upload.
4. GitHub Actions validates the archive, extracts it to `apps/<slug>/`, removes the incoming archive, updates `apps.json`, and publishes GitHub Pages.
5. Monitor **Actions → Build and deploy AppHub**.

ZIP requirements:
- `index.html` at the archive root or one folder deep.
- Dashboard upload limit: 20 MB.
- Expanded archive limit: 100 MB and 4,000 files.
- Symbolic links and unsafe paths are rejected.
- A valid upload using an existing slug replaces that app.

Security:
- Token remains in page memory only and is not stored in browser storage or repository.
- Token is sent to GitHub API over HTTPS.
- Uploaded app source and assets are public on this public Pages site.
- Never upload secrets or server-side credentials.
