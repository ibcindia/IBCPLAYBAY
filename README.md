# IBC Play BAY – OTT Channel Website

- `index.html` – public video gallery (no registration, anyone can watch)
- `admin.html` – admin panel to upload and delete videos
- `videos.json` – the video list (the admin panel edits this for you)
- `style.css` – shared design

## Setup (one time)

1. Create a new GitHub repository, for example `ibc-play-bay`. Make it **Public**.
2. Upload all files from this folder to the repository root.
3. Go to **Settings → Pages**. Under Source choose **Deploy from a branch**, pick `main` and `/ (root)`, then Save.
4. After a minute your site is live at `https://YOURNAME.github.io/ibc-play-bay/`.
   - Gallery: `/`
   - Admin: `/admin.html`

## Create the admin token

1. GitHub → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. Repository access: **Only select repositories** → choose `ibc-play-bay`.
3. Permissions → Repository permissions → **Contents: Read and write**.
4. Copy the token (starts with `github_pat_`).
5. Open `/admin.html`, enter `YOURNAME/ibc-play-bay` and the token, then click **Connect**.

The token is stored only in your browser. Visitors who open `admin.html` see the connect form and cannot do anything without it. Never share the token.

## Adding videos

- **Upload a file**: .mp4 or .webm, under 50 MB each.
- **YouTube link**: best for long episodes. Upload as Unlisted on YouTube, paste the link.
- **Direct link**: any public .mp4 URL (for example from Cloudflare R2 or Bunny.net).

After publishing, the gallery refreshes in about one minute.

## Limits to know

GitHub Pages is free static hosting. Keep the repository under about 1 GB and monthly traffic under about 100 GB. For many full-length episodes, host the video files on YouTube, Cloudflare R2 or Bunny.net and use the link option. The admin panel and gallery work the same way.
