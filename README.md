# Fanisi Digital website

Source and published static files for https://fanisidigital.co.ke/.

## Build

Requires Python 3. Run from the repository root:

```sh
python source/catalogue/build.py
```

## Preview

```sh
python -m http.server 8080 --directory dist
```

Open http://localhost:8080/. Deploy the contents of `dist/` to a static host. Python is only required to regenerate pages, not to serve them.

## Checks

```sh
python checks/check_inventory.py
node checks/check_catalogue.cjs
node checks/check_enquiry.cjs
node checks/check_analytics.cjs
```

## Editing

- `source/catalogue/laptops.txt`: supplied inventory prices; the generator adds KSh 3,000 once.
- `source/catalogue/build.py`: shared pages, catalogue and navigation.
- `source/catalogue/design_refinement.py`: homepage layout.
- `source/catalogue/website_pages.py`: website services.
- `source/catalogue/search_content.py`: search-focused pages and structured data.
- `dist/assets/site.css`: styles using the Fanisi palette.
- `dist/assets/`: scripts, logo and product images.

Google Analytics is consent-gated. Enquiry forms prepare a WhatsApp message; users choose whether to send it.

## Hosting

This repository is a copy of the current website source. Uploading it does not move the existing live hosting or automatically enable GitHub deployment. `.openai/hosting.json` retains the existing Sites project reference.
