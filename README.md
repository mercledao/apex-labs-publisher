# Apex Labs publisher website

A static, responsive publisher directory for **Apex Labs Pte Ltd**, featuring Mercle and Distracted. No framework, package installation, database, cookies, analytics, or build step is needed.

## Preview locally

Run from this directory:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Open http://127.0.0.1:4173/. All app, support, and legal links are ordinary HTML links and the site works with JavaScript disabled.

## Publish on GitHub Pages after local review

1. Put this folder's contents at the root of a new repository, such as `apex-labs-publisher`, with `main` as the default branch. Prefer the company's GitHub organization.
2. In the repository, open **Settings → Pages → Build and deployment** and select **GitHub Actions**.
3. Run the **Publish GitHub Pages** workflow, or push to `main`. The included workflow publishes only `index.html`, `styles.css`, `.nojekyll`, and `assets/`.
4. Open the HTTPS URL returned by the deployment. A project repository normally uses `https://<owner>.github.io/<repository>/`. A repository named `<owner>.github.io` uses `https://<owner>.github.io/`.
5. Verify the published page and all outbound URLs in a signed-out browser, then update the publisher **Website** in the Solana Mobile portal to the deployed URL.

The relative asset paths work at either an account root or a project subpath. The page has no private account or sign-in dependency. A custom domain can be added later.

## Edit content

- Publisher identity, app details, support emails, and policy URLs: `index.html`.
- Colors, typography, and responsive layout: `styles.css`.
- Existing official app icons: `assets/mercle.png` and `assets/distracted.jpg`.
- To add an app, copy an `<article class="app-card">` block and update its unique heading ID, name, icon, description, and links. Update the app count, meta description, and any two-app wording.

## Content and policy notes

- Publisher identity: `Apex Labs Pte Ltd`.
- Mercle website: https://mercle.ai/
- Mercle support: support@mercle.xyz (from its public listing).
- Mercle privacy: https://mercle.ai/privacy (also referenced in the Mercle app).
- Distracted website: https://distracted.bet/
- Distracted support: hey@distracted.bet (from its existing Seeker listing).
- Distracted privacy: https://distracted.bet/privacy-policy
- Distracted terms: https://distracted.bet/terms-of-use
- The former Distracted listing URL `/tos` serves the game rather than a policy. Use the current policy URLs above.
- No separate Mercle terms page has been verified. `https://mercle.ai/terms` returned 404 on 26 October 2026; it has deliberately not been linked. Confirm the correct Mercle terms URL before preparing a new app submission.
- The site links existing app policies; it does not invent or replace their legal text. The new publisher URL is separate from the app-specific website and policy URLs in each app listing.

Solana Mobile requires a public publisher website and separate public HTTPS terms/privacy pages for app submission: https://docs.solanamobile.com/dapp-store/submit-new-app

Publication is handled by the included GitHub Pages workflow.
