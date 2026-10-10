# MyAssist Network (www.myassistnetwork.com)

Private "vault" entrance site: wide vault image, tap, walk-up video, PRESS TO UNLOCK, unlock clip into light, project hub.
Owned by 2451842 Alberta Inc. MyAssist is TM (filed, not registered), never (R).

## Hosting
- GitHub Pages from `main`, root. Pushing to `main` updates the live site.
- Plain static site: `index.html` plus `img/`, `video/`, `audio/`. No build step.

## DNS (Network Solutions) - do not let records clash
- `@` (4 A records 185.199.108-111.153) and `www` (CNAME to nglives4ever-blip.github.io) -> GitHub Pages (this repo)
- `yodi` (CNAME) -> Vercel, for YODI. Separate app, separate repo (nglives4ever-blip/yodi). Never delete or change it.
- `canba` subdomain -> Canba tracker. Never delete or change it.

## Rules
- YODI is not built in this repo.
- Any login or database for this site uses the Supabase project "myassist-network", never "myassist" (that is the Autolink MyAssist app).
- Never put a Supabase service_role key or any API key in the page. The anon public key is fine.
- Phone-first, then desktop. Show a mockup before UI changes. No em dashes in written content.
