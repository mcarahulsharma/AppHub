# AppHub

A personal web application launcher for GitHub Pages. Applications are deployed by uploading ZIP archives from the AppHub dashboard; GitHub Actions validates and publishes each app.

## Setup
1. Upload the contents of this folder to the root of your public `AppHub` repository.
2. In GitHub, open **Settings → Pages** and select **GitHub Actions** as the build and deployment source.
3. Ensure **Settings → Actions → General → Workflow permissions** allows read and write permissions (the workflow commits validated app files and updates the registry).
4. Open the Pages URL shown in repository Settings → Pages.

See `docs/DEPLOYMENT.md` and `docs/HOME-ASSISTANT.md`.

**Important:** GitHub Pages is public static hosting. Uploaded apps and their source/assets become public. Do not upload secrets or private data.
