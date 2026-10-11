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

## Look-around
- Phones: drag pans the wide shot left/right (natural direction), release drifts back to center; the room auto-drifts gently with a "Take a look around" hint until touched, and again after idle.
- Future 360 room (planned, 30 ft ceiling): up/down is INVERTED (drag down looks up, drag up looks down). Left/right stays natural, never inverted.

## Home page = the look-around (live since Oct 11 2026)
- `index.html` is a copy of `lookaround/index.html` with `<base href="/lookaround/">` so all its relative paths still resolve, title "MyAssist Network", no noindex, no "Vault" back button, no "Look around · test" tag.
- Workflow: build and approve changes on /lookaround/ first, then re-copy to `index.html` keeping those four differences.
- The old front flow (vault image, walk-up, unlock) is kept as `classic.html`, not linked.

## /lookaround/ test page (lookaround/index.html) - test bench for the home page
Canvas frame-scrub built from Johnny's Veo clips.
- Turn (h/, 168 frames; hm/ = 960px phone copies): drag is 1:1 with the cursor using measured per-frame shift (D/S arrays), frames slide and cross-fade. Stops: vault (frame 0) and lobby (82). Past LIMIT the camera takes over (glitch on the right route). Lobby rests on the HD still lobby.jpg, aligned to frame 82 (HD_M).
- Look up (v/, vm/): only from the vault. Stations: vault, sign from below (88, auto stops here going up), sign close-up (97, auto stops here coming down), ceiling (185). 88 to 97 is under the hand.
- Release: after 2s eases back to the current station. Lobby, sign and ceiling are stations: user must move back on their own.
- Vault tips (#tip): 5s idle at the vault shows one random pill pinned to the kiosk's lower panel above TAP TO ENTER (kBox from draw(), TIP_AT 0.62) (look up / look around / move right / move left), never the same twice running, nudging gold chevrons; any touch hides it. Replaced the old bottom "drag to look around" hint, which now only carries the step-back cue. Test hook window.__tip().
- Sound: glitch 0.55, other effects 0.6, hum 0.2. Sound always starts on (mute lasts one visit). Cosmic film plays audio/ring-splash.mp3 (Johnny's shimmer) at 2.1s at 0.38 with fade in/out, reversed on the way back.
- Posters (tracked quads 78-118): click plays a film starting on the HD lobby (freedom.*, cosmic.*), short soft glitch over the AI wobble, click again plays the *_rev film back to the lobby.
- Kiosk: click plays ../video/walkup (starts exactly on frame 0), PRESS TO UNLOCK, ../video/unlock, Coming Soon, back to vault.
- Cursors: gold open hand, fist only while grabbing the room, gold pointing finger (hand-point*.png) over posters/kiosk/press (never a fist there).
- Phone (portrait): free look inside the frame first (left/right, a little up/down), overflow turns the footage (PH_GAIN 2, long limits x0.6), flick glide, 1x canvas, no grab zoom, lobby left edge holds then a firm pull goes to the vault (avoids the baked glitch frames). TAP TO VIEW / TAP TO ENTER breathing gold cues; press lights the target. During a poster film the step-back cue moves to the top on phones (level with the sound button, "Tap anywhere to step back"); desktop keeps it at the bottom as "Click".
- Test hooks: window.__la(), __pa(x,y), __pb(). Test with Playwright; python http.server lacks Range requests so videos can't seek, use a Range-capable server.
- Always give Johnny the link at the end: https://www.myassistnetwork.com/lookaround/

## Rules
- YODI is not built in this repo.
- Any login or database for this site uses the Supabase project "myassist-network", never "myassist" (that is the Autolink MyAssist app).
- Never put a Supabase service_role key or any API key in the page. The anon public key is fine.
- Phone-first, then desktop. Show a mockup before UI changes. No em dashes in written content.
