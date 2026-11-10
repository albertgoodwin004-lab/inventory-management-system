# Architecture / CSS Style Guide

This application is intentionally static. It has no JavaScript folder, script references, dynamic handlers, servers, or runtime dependencies.

- `assets/css/main.css`: global color tokens, typography, cards, buttons, shared forms, and tables.
- `assets/css/index.css`: sidebar, shared shell, responsive navigation, active link appearance.
- `assets/css/dashboard.css`: dashboard cards, quick actions.
- `assets/css/stock.css`: stock register.
- `assets/css/add.css`: add-item form.
- `assets/css/suppliers.css`: supplier form and directory.
- `assets/css/reports.css`: stock reporting.

All pages link using relative HTML `href` attributes (no iframe, no JavaScript). Every page contains its own navigation markup so the current page can have a correct `aria-current="page"` and active style.

**Do not add JavaScript** unless project requirements explicitly change. Forms are examples and their submit buttons are disabled to avoid falsely suggesting that data was saved.

## Login and Logout

`index.html` is the landing page and uses `assets/css/login.css`. Its required username/password fields submit to `dashboard.html` without using JavaScript or storing credentials. Every workspace page has a Logout link back to `index.html`. These links are demonstrations, not secure sessions or access control.
