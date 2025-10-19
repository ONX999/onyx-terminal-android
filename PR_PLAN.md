# PR: Add validate-secrets workflow

This PR adds a manual GitHub Actions workflow to verify that the required repository secrets are present for Android release signing and Google Play Internal publishing.

Secrets checked:
- `SIGNING_KEYSTORE_BASE64`
- `SIGNING_KEY_ALIAS`
- `SIGNING_KEY_PASSWORD`
- `KEYSTORE_PASSWORD`
- `PLAY_SERVICE_ACCOUNT_JSON`

How to use:
1. Go to Actions → "Validate required Secrets"
2. Click "Run workflow"
3. The job will fail and list any missing secrets, or succeed if all are present.
