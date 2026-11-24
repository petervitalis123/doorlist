# Doorlist

Party and event ticketing prototype: events, pageantry, voting, vendors.
One self-contained file: `index.html`. No build step.

Test mode only. No real payments are taken. On a normal host the data stays in each
visitor's own browser (local mode); sharing data between people needs a real server.

## Deploy on Render
1. Render dashboard > New > Static Site > pick this repo.
2. Build command: leave empty. Publish directory: `.`
3. Create Static Site. Open the URL Render gives you.

## Short links
Short links such as `yoursite.com/miss-campus` work because `render.yaml` rewrites every path to
`index.html`. If you create the Static Site by hand instead of from `render.yaml`, add a rewrite
rule in the Render dashboard (Redirects/Rewrites): source `/*`, destination `/index.html`, action Rewrite.

## What this test version cannot do yet
- It cannot send email, text or WhatsApp messages. Update sign-ups are collected only.
- Student, presale, per-person limits and door sales are checked in the visitor's browser. Real
  enforcement needs a server.
- Events and sign-ups live in each visitor's own browser here, so a link opens correctly only on the
  device that created the event until a shared database is added.
- Apple and Google Wallet passes need signing certificates and a server. "Save ticket image" is the stand-in.
- The sign-up wording needs legal review (for example NDPR in Nigeria, GDPR in the UK and EU).
