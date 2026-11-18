# Publish the privacy policy to GitHub Pages

`index.html` in this folder is the GitHub Pages-ready copy of
`../domino_shak_app/PRIVACY_POLICY.html`. It is self-contained (inline CSS/JS,
no external assets), shows Arabic and English, and has a canonical link to the
target URL. **Nothing has been published yet.**

- Repository: https://github.com/Ali-Ashraf-Saad/dominoshak-privacy
- Target URL: https://ali-ashraf-saad.github.io/dominoshak-privacy/
- Developer name: Domino Shak / دومينو شك
- Support email in the policy: dominoshak.support@gmail.com

## Publish with the GitHub web UI (simplest)

1. Sign in to GitHub and open https://github.com/Ali-Ashraf-Saad/dominoshak-privacy.
2. Click **Add file → Create new file**.
3. In the filename field type exactly `index.html` (repository root, no folder).
4. Open `privacy_site/index.html` from this workspace in a text editor, select all, and paste the entire content into the file body.
5. Commit message: `Add Domino Shak privacy policy`. Choose **Commit directly to the `main` branch**, then click **Commit new file**.
   - If the repository's default branch is `master`, use that branch and select it again in step 8.
6. In the same repository open **Settings → Pages**.
7. Under **Build and deployment → Source**, select **Deploy from a branch**.
8. Under **Branch**, choose **`main`** and **`/ (root)`**, then click **Save**.
9. Wait for the green banner "Your site is live at https://ali-ashraf-saad.github.io/dominoshak-privacy/". HTTPS activation can take a minute.

## Alternative: publish from a terminal with git

```bash
git clone https://github.com/Ali-Ashraf-Saad/dominoshak-privacy.git
cd dominoshak-privacy
cp /home/ali/Documents/DominoGame/privacy_site/index.html ./index.html
git add index.html
git commit -m "Add Domino Shak privacy policy"
git branch -M main
git push -u origin main
```

Then complete steps 6–9 above (Settings → Pages → Deploy from a branch → `main` / `/ (root)` → Save).

## Verify after publishing

- Open https://ali-ashraf-saad.github.io/dominoshak-privacy/ in an incognito/private window.
- Confirm HTTPS with no certificate warning, both languages render, the language buttons work, and section 11 shows `Domino Shak` / `دومينو شك`, `dominoshak.support@gmail.com`, and the URL above.
- Confirm the support email link opens a mail composer.
- Tell the agent that the page is publicly accessible over HTTPS. **Only then** decide whether to rebuild the AAB. Do not upload anything to Google Play without separate explicit approval.

## Why a hosted copy is needed

Play Console requires a public HTTPS privacy-policy URL. A local or in-app-only copy cannot satisfy that. `domino_shak_app/assets/web/PRIVACY_POLICY.html` remains the in-app copy served from `http://localhost:8080`; this hosted copy is for the Play listing and the Play Console privacy-policy field.
