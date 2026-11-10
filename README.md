# Inventory Management System — HTML & CSS Only

A clean, responsive **static user-interface prototype** made exclusively with HTML and CSS. No JavaScript, no frameworks, no database, and no external runtime dependencies.

## Run locally

Download or clone this repository, then open `index.html` in a web browser. The login screen accepts any non-empty username and password and takes you to `dashboard.html` as a visual demonstration. You can also use any static file hosting service, including GitHub Pages.

## Pages

| File | Purpose | Dedicated CSS |
| --- | --- | --- |
| `index.html` | Login page (site entry point) | `login.css` |
| `dashboard.html` | Dashboard overview | `index.css`, `dashboard.css` |
| `stock.html` | Example stock register | `stock.css` |
| `add-item.html` | Add-item form mockup | `add.css` |
| `suppliers.html` | Supplier directory and form mockup | `suppliers.css` |
| `reports.html` | Example report | `reports.css` |

Every page loads `assets/css/main.css` (shared colors, buttons, forms and tables). Workspace pages also load `assets/css/index.css` (sidebar and responsive navigation). The login screen loads `assets/css/login.css` instead.

## What works

- Each navigation link opens the correct HTML page, including direct links between pages.
- The Login form opens the dashboard when both fields are filled. Logout returns to the login page.
- The active page is styled without scripts.
- The layout adjusts for smaller screens using CSS media queries.
- Input validation and reset controls use native HTML behavior.
- Icons are inline SVG markup (they need no icon library or JavaScript).

## Login and security

Login and Logout are visual navigation only. **They do not authenticate or protect pages.** Any non-empty credentials are accepted, and dashboard pages can still be opened directly. No credentials are stored or sent as query parameters. Real authentication requires server-side code, which is intentionally out of scope for an HTML/CSS-only project.

## Static prototype limitations

- **Add Item / Save Supplier:** Buttons are intentionally disabled because there is no storage backend; form fields are visual demonstrations only.
- **Stock filter:** Disabled, since filtering rows requires logic outside HTML/CSS in this design.
- **Dashboard and reports:** Sample values, not live counts.
- **Suppliers:** Read-only example contacts; no add/edit/delete storage.

Do not represent this as a working inventory-management backend. For this version the project uses **HTML and CSS only**, as requested.

## Structure

```text
inventory-management-system/
├── index.html
├── dashboard.html
├── stock.html
├── add-item.html
├── suppliers.html
├── reports.html
├── assets/
│   └── css/
│       ├── main.css
│       ├── login.css
│       ├── index.css
│       ├── dashboard.css
│       ├── stock.css
│       ├── add.css
│       ├── suppliers.css
│       └── reports.css
├── docs/
│   └── STRUCTURE.md
├── .gitignore
└── README.md
```

## Customizing colors

Change the variables at the top of `assets/css/main.css` to update the same palette everywhere. Change layout structure in `index.css`; page-specific styling belongs only in its matching stylesheet.

## Publish on GitHub

```bash
git init
git add .
git commit -m "Build static HTML and CSS inventory interface"
git branch -M main
git remote add origin YOUR_REPOSITORY_URL
git push -u origin main
```

For GitHub Pages, select **Settings → Pages → Deploy from a branch → main / root**.
