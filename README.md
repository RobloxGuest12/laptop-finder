Laptop Finder
A static, GitHub Pages-friendly laptop finder prototype.
Files
`index.html` — responsive website and survey/filter interface
`laptops.json` — starter laptop catalog
Run locally
Because the page loads `laptops.json` with `fetch`, run it through a local web server rather than opening `index.html` directly.
For example, with Python installed:
```bash
python -m http.server 8000
```
Then visit http://localhost:8000.
Publish on GitHub Pages
Create a GitHub repository.
Upload `index.html` and `laptops.json` to the repository root.
Open Settings → Pages.
Choose Deploy from a branch, select `main` and `/ (root)`, then Save.
Open the published Pages URL after deployment finishes.
Important data limitations
This is a working prototype with a small demonstration catalog, not a complete worldwide laptop database. Some catalog entries describe model families rather than exact SKUs. Example prices and retailer search links are illustrative and are not live offers or verified availability.
For a real worldwide service:
Add exact model/SKU records and verify specs against manufacturers.
Integrate authorized retailer/affiliate APIs or licensed product feeds.
Keep marketplace offers separate from laptop model records.
Store price currency, seller, condition, country, shipping destination, warranty, URL and `last\_checked` timestamp for each offer.
Never put private API keys in frontend JavaScript or a public GitHub repository. Use a backend/serverless function for APIs that require secrets.
Respect each marketplace's terms, API limits and data licensing. Do not scrape sites without permission.
Add currency conversion and shipping/tax estimates only when reliable regional data is available.
Shopee is included as a marketplace choice in the starter catalog. Regional Shopee sites and live offers need their own supported integrations; search links are only examples.
