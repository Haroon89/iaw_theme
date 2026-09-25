# iaw_theme

The Saudagar desk theme for stock Frappe v16 / ERPNext v16: colours, fonts,
radii, shadows, control styling and the dark theme — **look and feel only**.

- One stylesheet: `iaw_theme/public/css/iaw_theme.css`, included for the desk
  (`app_include_css`) and website pages including login (`web_include_css`).
- Self-hosted fonts (variable woff2, SIL OFL licences in `licenses/`):
  Plus Jakarta Sans (text), Baloo Bhaijaan 2 (display, for later JS phases),
  Noto Nastaliq Urdu (Urdu, for later JS phases). No Google Fonts at runtime.
- No doctypes, no fixtures, no JS, no layout changes — it can be removed on
  its own (`bench --site <site> uninstall-app iaw_theme`).

Every colour, size, radius and shadow value comes from the Saudagar design
tokens (`docs/design-system/tokens/tokens.css` in the `saudagar-deploy`
repo): light theme on `:root,[data-theme="light"]`, dark on
`[data-theme="dark"]` — the selector Frappe v16 actually uses (rendered on
`<html>` from the user's `desk_theme`).
