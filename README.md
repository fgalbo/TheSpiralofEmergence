# Spiral of Emergence – Scroll Experience

A lightweight, single‑file Web 3.0 “scrollytelling” site that pairs illustrated chapter title cards with full narrative text.

---

## File structure

    spiral_complete/
    └── index.html   ← self‑contained page (images embedded as Base‑64)

*(No external CSS, JS, or image files are required.)*

---

## Live preview

1. **Open locally**

       open index.html        # macOS
       start index.html       # Windows
       xdg-open index.html    # Linux

2. **Scroll**

   Each viewport‑height section snaps in place:  
   1. Chapter artwork  
   2. Quote slide  
   3. Full chapter prose slide  

---

## Customization cheatsheet

| What to edit            | Where / how                                                                                  |
| ----------------------- | -------------------------------------------------------------------------------------------- |
| Star density / opacity  | Edit the `opacity:` or dot‑count in the base‑64 noise PNG inside the `<style>` block         |
| Fonts / sizing          | Tweak CSS rules for `body`, `.textwrap p`, and media queries                                 |
| Swap artwork            | Replace the base‑64 string after `src="data:image/jpeg;base64,`                              |
| Add parallax / motion   | Attach a `@keyframes` translate animation to `body::before` or `.imageonly img`             |

---

## One‑click deployment

| Platform              | Free tier                        | Steps                                                                              |
| --------------------- | -------------------------------- | ---------------------------------------------------------------------------------- |
| **Netlify**           | Unlimited sites, 100 GB transfer | Drag‑and‑drop `index.html` on <https://drop.netlify.com> → follow custom‑domain UI |
| **Vercel**            | Unlimited static, 100 GB         | `vercel deploy --prod` or connect GitHub repo                                      |
| **Cloudflare Pages**  | Unlimited static bandwidth       | Push to Pages via Git or direct upload                                             |
| **Fleek** (IPFS)      | 1 GB free                        | Fleek Dashboard → drop file → ENS / IPFS CID output                                |

---

## Custom domain quick start

1. Register **spiralofemergence.io** (Namecheap, Porkbun, or Cloudflare Registrar).  
2. Deploy to Netlify (or Vercel).  
3. Copy the two DNS records Netlify provides into your registrar’s DNS panel.  
4. Wait 5–30 minutes for propagation; HTTPS auto‑activates.

### Web 3.0 mirror (optional)

    # Pin to IPFS (Pinata, Fleek, or local node)
    ipfs add index.html -w

    # Set ENS content hash
    set-contenthash spiralofemergence.eth <CID>

Now the site resolves at `spiralofemergence.eth.link` and in any Web3‑enabled browser.

---

## License

| Part            | License                             |
| --------------- | ----------------------------------- |
| Code & CSS      | MIT                                 |
| Prose & Artwork | Creative Commons BY‑NC‑SA 4.0       |

Feel free to fork the project, build on the code, and remix the narrative/graphics non‑commercially as long as you credit the original and license derivatives under the same terms.
