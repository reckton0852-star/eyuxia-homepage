# Eyuxia Homepage

This repository is the main maintenance repo for the `eyuxia.xyz` personal website.

It is used for:

- homepage structure and visual updates
- project showcase content
- copywriting and profile updates
- static asset management
- deployment updates for the main site

## Site Role

- main site: `eyuxia.xyz`
- optional alias: `www.eyuxia.xyz`
- stock proxy service: `stock.eyuxia.xyz`

This repo is only for the main website.
The stock proxy and device firmware belong to their own project repos.

## Project Structure

- `index.html`: homepage entry
- `styles.css`: main site styles
- `assets/`: images and other static assets
- `DEPLOY_TO_CLOUDFLARE_PAGES.md`: deployment notes

## Local Preview

This is a static site.
You can open `index.html` directly in a browser for a quick preview.

## Deployment

Recommended deployment target:

- Cloudflare Pages or Workers static hosting
- custom domain: `eyuxia.xyz`

Recommended domain split:

- `eyuxia.xyz` -> homepage
- `www.eyuxia.xyz` -> homepage alias
- `stock.eyuxia.xyz` -> stock ticker proxy service

## Maintenance Note

When working in this repo, treat it as the primary branch for `eyuxia.xyz` website maintenance.
Other hardware or firmware work should stay decoupled unless it directly affects the website content.
