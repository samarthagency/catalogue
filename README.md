# Medical Product Catalogue — GitHub Pages

A responsive, mobile-friendly catalogue website for a medical distribution business. Each product card opens its own PDF brochure, and the first page of each PDF is used as a preview when the browser can load it. It includes search, category filters, WhatsApp enquiry and click-to-call links.

## Quick start

1. Download and unzip this folder.
2. Open `products.js` in a text editor.
3. Replace `Your Business Name`, `phoneDisplay` and `phoneDigits` with your details.
   - `phoneDigits` must contain country code + number, digits only. Example format for India: `919876543210`.
4. Put your PDFs inside the `brochures` folder.
5. In `products.js`, replace the six sample products with your real products. For each product, set:
   - `name`: product or machine name
   - `brand`: brand/manufacturer
   - `category`: e.g. `Hematology`, `Biochemistry`, `Coagulation`, `Electrolytes`, `Glucometers`, `Reagents & Consumables`
   - `description`: a short line
   - `pdf`: the exact path, e.g. `brochures/my-machine.pdf`
6. Save your files.

### File naming tips

Use short file names with lowercase letters, numbers and hyphens. Avoid spaces and special characters. The file name in `products.js` must exactly match the actual PDF name.

Example:
```js
{
  name: "3-Part Hematology Analyzer",
  brand: "Example Diagnostics",
  category: "Hematology",
  description: "Compact analyzer for routine CBC testing.",
  pdf: "brochures/3-part-hematology-analyzer.pdf"
}
```

## Test locally

The website uses PDF.js from a CDN to render the first page of brochures. Because browsers may restrict PDF loading when you open `index.html` directly from your computer, test with a local server.

If you have Python installed, open a terminal in this folder and run:
```bash
python -m http.server 8000
```
Then open `http://localhost:8000`.

If PDF previews do not appear locally, the brochure links can still work. Check the file path and test after publishing to GitHub Pages.

## Publish for free with GitHub Pages

1. Sign in to GitHub and create a **public repository**, e.g. `medical-product-catalogue`.
2. Upload `index.html`, `style.css`, `app.js`, `products.js`, `README.md`, and the `brochures` folder with your PDFs.
3. Open the repository's **Settings → Pages**.
4. Under build and deployment, select **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then save.
6. Wait for GitHub Pages to publish the site. The URL will look like `https://YOUR-USERNAME.github.io/medical-product-catalogue/`.

## Important notes

- GitHub Pages repositories are public. Only upload brochures and product information you are allowed to distribute publicly.
- GitHub has file-size limits and repository size recommendations. If a PDF is too large, host that PDF on a suitable file-sharing service and use its public URL as the `pdf` value, or reduce the PDF size. Check GitHub's current limits before uploading many large brochures.
- This is a static website: it does not store enquiries or customer data. WhatsApp and call buttons open the visitor's own phone/app.
- Do not publish patient information or confidential documents.
- Update the sample products before sharing the link with doctors.


## Samarth Agency details

Edit `window.CATALOGUE_CONFIG` in `products.js` to set your business name, full address, email, primary phone number, optional additional phone numbers and About Us paragraph. Use country code + phone number as digits only for `phoneDigits` (for example, `919876543210`). Replace all placeholder details before publishing. The feature strip below the hero has been removed.


## Wide-screen layout update

The latest CSS update expands the desktop content area, makes the hero more spacious, and uses four product cards per row on wide monitors. Tablet and mobile layouts remain responsive.
