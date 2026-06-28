# Deploy Homepage to Cloudflare Pages

This guide assumes:

- your domain `eyuxia.xyz` is already managed by Cloudflare
- your stock proxy is already using `stock.eyuxia.xyz`
- this homepage should become the main site at `eyuxia.xyz`

---

## 1. Prepare a GitHub Repository

Create a new GitHub repository for the homepage, for example:

- `eyuxia-homepage`

Recommended files to upload:

- `index.html`
- `styles.css`
- `README.md`
- `assets/esp32-stock-ticker-demo.jpg`

You can keep the homepage as a simple static site.

---

## 2. Upload the Homepage Files

The current homepage folder is:

- `C:\Users\reckt\Documents\ESP32-weixue-1.4inch\homepage`

Upload the contents of this folder to your new GitHub repository.

Recommended structure in the repo:

```text
/
  index.html
  styles.css
  README.md
  assets/
    esp32-stock-ticker-demo.jpg
```

---

## 3. Create a Cloudflare Pages Project

In Cloudflare:

1. Go to `Workers & Pages`
2. Click `Create`
3. Choose `Pages`
4. Connect to Git
5. Select your new homepage GitHub repository

Because this is a static site, use settings like:

- Framework preset: `None`
- Build command: leave empty
- Build output directory: `/`

Then deploy.

---

## 4. Bind the Custom Domain

After the first successful deployment:

1. Open the Pages project
2. Go to `Custom domains`
3. Add:
   - `eyuxia.xyz`
4. Optionally also add:
   - `www.eyuxia.xyz`

Cloudflare will usually create the needed DNS records automatically if the domain is already in the same account.

---

## 5. Keep the Stock Proxy Separate

Your stock proxy can continue to use:

- `stock.eyuxia.xyz`

This means:

- homepage: `eyuxia.xyz`
- stock proxy API: `stock.eyuxia.xyz`

That separation is clean and recommended.

---

## 6. Suggested Final Structure

Suggested public structure:

- `https://eyuxia.xyz/`
  - personal homepage
- `https://eyuxia.xyz/projects/esp32-stock-ticker`
  - future project detail page
- `https://stock.eyuxia.xyz/`
  - stock proxy API

Right now, the current homepage is a single-page site. You can expand it later.

---

## 7. Recommended Next Improvements

After the homepage is online, the next useful upgrades are:

1. Add more project cards
2. Add a dedicated detail page for `ESP32 Stock Ticker`
3. Add real photos for each project
4. Add a short About / Contact section
5. Add bilingual content if needed

---

## 8. Quick Checklist

- [ ] create GitHub repo for homepage
- [ ] upload homepage files
- [ ] create Cloudflare Pages project
- [ ] deploy static site
- [ ] bind `eyuxia.xyz`
- [ ] verify homepage opens normally
- [ ] verify `stock.eyuxia.xyz` still works

