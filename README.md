# Center for Biblical Missions · Content Generator (Portal)

English-language landing page for CBM's content-repurposing workflow. Single-file static page that wraps the two n8n form URLs (Upload + Generate) in a clean, on-brand interface.

Live: _add GitHub Pages URL after first push_

## What it does

A CBM-styled portal with three tabs:

- **Start**, three action cards (Upload Source, Generate Content, Make a Graphic) that open the n8n forms and graphic generator in a new tab.
- **Guide**, five-step usage walkthrough.
- **About**, what the tool does, how it stays faithful to the source, and CBM's missions framing.

## Wired-in n8n endpoints

- Upload form: `TODO, set after the CBM workflow is published`
- Generate form: `TODO, set after the CBM workflow is published`

Once the n8n workflow is cloned and published, fill in the two `<a class="card-cta" id="btn-upload"|"btn-generate">` `href` attributes in `index.html`.

## Design DNA

Pulled from [cbm.tmai.org](https://cbm.tmai.org):

| Token | Value | Source |
|---|---|---|
| Light background | `#FFFFFF` | Gurgen's request (white) |
| Dark background | `#1B1D21` | cbm.tmai.org article pages |
| Primary accent | `#114D5D` | cbm.tmai.org Books page (navy) |
| Accent hover (light) | `#1A6E84` | brighter navy |
| Accent deep | `#0B2F39` | deepest navy for headlines |
| Warm secondary (dark only) | `#EE6D49` | cbm.tmai.org primary CTA terracotta |
| Heading font | Inter (700/800) | clean modern, matches cbm.tmai.org sans aesthetic |
| Body font | Inter | same family |
| Mono font | DM Mono | for eyebrows and metadata |

## Run locally

```bash
cd cbm-portal-v1
python3 -m http.server 8766
# open http://127.0.0.1:8766/
```

## Deploy to GitHub Pages

```bash
# After creating empty repo "cbm-portal-v1" on GitHub
git remote add origin https://github.com/J4m3sdev/cbm-portal-v1.git
git branch -M main
git push -u origin main
# Settings, Pages, Source = main, folder = / (root), Save
```

## Files

- `index.html`, the entire portal (HTML, CSS, JS)
- `generator/index.html`, the graphic generator
- `og.png`, `og.svg`, social-card preview assets
- `assets/cbm-logo.{svg,png}`, brand logo (drop in when received)
- `README.md`, this file

## Lineage

Sibling project to:
- `didasko-portal-v1`, the Czech partner clone this was forked from
- n8n workflow `<TODO-cbm-workflow-id>` (CBM Content Repurposer), the backend the cards link to
