# RoSo Wedding Planner

Seating arranger, guest data editor and drinks calculator for Ronan & Sophia's wedding.

- **Site:** https://ronanheal.github.io/roso-wedding-planner/
- **Data:** `data.json` on the [`data` branch](../../tree/data). Every save from the site is a commit there, so the branch history is a full undo log.

## How access works

Anyone with the site link can **view**. To **edit**, the site needs a GitHub key with write access to this repo only. The key is never stored in the repo. It lives in each editor's browser after they open an editor link once.

### Make the edit key (once)

1. GitHub → Settings → Developer settings → Personal access tokens → **Fine-grained tokens** → Generate new token.
2. **Repository access:** Only select repositories → `roso-wedding-planner`.
3. **Permissions → Repository permissions → Contents:** Read and write. Leave everything else as is.
4. Set an expiry after the wedding, generate, and copy the token.
5. Open the site, click **Edit access**, paste the token and click **Unlock editing**.
6. Click **Copy editor link** and send that link to anyone who should edit. Opening it unlocks editing on their device.

If the key leaks, the worst anyone can do is change this repo. Delete the token on GitHub and make a new one to cut off access.

## Rolling back a bad change

Find the commit on the `data` branch, open `data.json` at that commit, and copy its contents back into the file on the branch (or `git revert` the commit).

## Files

- `index.html`: the whole app (no build step).
- `data.json` (on `data` branch): guests, seating, saved plans, drinks budget and settings.
