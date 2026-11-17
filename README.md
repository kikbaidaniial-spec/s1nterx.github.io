# Alem English website

## GitHub Pages

Upload `index.html` and `2hollis - crush (official visualizer).mp4` to the repository root, then enable Pages from the `main` branch and `/(root)`.

## Private email form endpoint

The form does not contain the recipient email. Deploy `worker/index.js` as a Cloudflare Worker and configure:

- Secret `RECIPIENT_EMAIL` with the inbox that should receive applications.
- Variable `ALLOWED_ORIGIN` with the site's origin, for example `https://YOUR-USERNAME.github.io` (without the repository path).

After deploying the Worker, replace `FORM_ENDPOINT` in `index.html` with its `workers.dev` URL, then commit the updated file to GitHub. The first form submission activates the inbox with FormSubmit; confirm the email it sends.