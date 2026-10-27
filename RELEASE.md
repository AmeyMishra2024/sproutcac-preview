# Sprout version 8: independent deployment snapshot

Prepared October 26, 2026 for the requested sproutcac.com copy.

## Exact source

- Existing Sites project: appgprj_6acea0a50a348191ab4a356872b6c4da
- Published version: 8
- Source commit: d83c8d72503dbaff397cf2e48a8d692493559778
- Existing public URL: https://sprout-congressional-app-challenge-2026.sunblazer-3166525679.chatgpt.site
- The existing deployment and domain settings have not been changed.

## Contents and verification

`dist/` contains all 54 static files from the clean, published source checkout. Every copied file was compared with its source using SHA-256 and matched. `sprout-v8-static.zip` packages this directory. `sprout-v8-source.bundle` preserves the source repository HEAD and its reachable history for recovery or a separate repository.

This is the browser-only public preview, with its existing lessons, practice trading, tutorial, parent demonstration and browser-local storage. It does not include the Flask account server or any private database. Practice saved under the old URL will not appear under a new domain because browser storage is separated by origin.

## Pending publication

No new deployment has been created, and sproutcac.com has not been configured. The Sites separate-copy operation is unavailable in the current session. A Render plugin connection has been offered as an alternate host. The domain currently uses Porkbun nameservers; DNS changes require authenticated access to its DNS settings.

For an independent static deployment, publish `dist` at the domain root. The client uses browser routes, so configure a fallback rewrite from unmatched paths to `/index.html` with status 200, while serving existing assets normally. Preserve the files in `dist` without rebuilding to reproduce this exact release. Disable automatic deployment from a development branch if this copy is intended to remain frozen.

After the independent service exists, add sproutcac.com to it, use only its returned DNS instructions, and verify HTTPS and the root and nested app routes before reporting completion. Preserve unrelated mail and verification records. Do not use the existing Sites deployment as a proxy or redirect, since that would not create an independent copy.

The hosting provider will assign new deployment identifiers and routing settings. The original Sites identity in the source bundle belongs to the old site and must not be reused to publish a separate Sites project.
