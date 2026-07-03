# kring-web

The **kring.cc** site. Starts as a single-file coming-soon page; migrates to Next.js + shadcn/ui + [21st.dev](https://21st.dev) components later (per the coded/own-it plan).

## Now: coming-soon page
`index.html` — a clean, single-file landing (KRING wordmark, email capture, subtle film grain). Colours/fonts come from `../Kring-Brand/tokens.json` (mirrored as CSS variables in the file).

## Deploy to kring.cc (Vercel)
1. Create a **GitHub repo** (`kring-web`) and push this folder.
2. In **Vercel**, "Add New Project" → import the repo → framework preset **Other** (it's static) → Deploy.
3. In Vercel → Settings → **Domains**, add `kring.cc`; point the domain's DNS (at your registrar) to Vercel per its instructions.
4. Done — every push to `main` redeploys.

## Wire the email capture (before launch)
The form currently shows a thank-you but doesn't store emails. To make it real:
- Connect **Brevo**, create a contact list + an embeddable form, and set the `<form>` `action`/`method` to Brevo's endpoint — or POST the email to Brevo from the inline script.

## Repo conventions
- `main` protected; feature branches; conventional commits.
- Secrets (API keys) in Vercel env vars — never commit them.
- Design tokens are the source of truth in `../Kring-Brand/tokens.json`.

## Next
Migrate to Next.js + Tailwind + shadcn/ui, import tokens, pull components from 21st.dev, keep the same wordmark + palette.
