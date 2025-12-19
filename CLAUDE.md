# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML website template for tree service businesses. Each HTML file is self-contained with embedded CSS - no build tools, bundlers, or external dependencies required.

## Template Customization

All HTML files use placeholder variables that must be replaced for each client:

| Placeholder | Description |
|-------------|-------------|
| `{{BUSINESS_NAME}}` | Company name |
| `{{CITY}}` | Primary city |
| `{{STATE}}` | State abbreviation (e.g., TX, NY) |
| `{{PHONE}}` | Business phone number |
| `{{EMAIL}}` | Contact email |
| `{{ADDRESS}}` | Street address |
| `{{AREA_1}}` - `{{AREA_5}}` | Service area towns/neighborhoods |

To customize for a new client, perform find & replace across all HTML files.

## File Structure

- `index.html` - Homepage (SEO target: company name + "[city] tree service")
- `tree-removal.html` - Service page (SEO target: "tree removal near me")
- `tree-pruning.html` - Service page (SEO target: "tree pruning/trimming")
- `land-clearing.html` - Service page (SEO target: "land clearing services")
- `stump-grinding.html` - Service page (SEO target: "stump grinding")
- `emergency-tree-service.html` - Service page (SEO target: "emergency tree service")
- `total lawn and tree website/` - Client images folder

## SEO Features

Each page includes:
- Schema.org LocalBusiness/Service/FAQPage JSON-LD markup
- Open Graph meta tags
- Geo meta tags for local SEO
- Proper H1/H2/H3 heading hierarchy
- Internal linking between all service pages

## CSS Customization

Colors are defined as CSS variables in `:root` at the top of each file's `<style>` block:
- `--primary-color` - Main green (#2d5a27)
- `--primary-dark` - Darker green (#1e3d1a)
- `--secondary-color` - Brown (#8b4513)
- `--accent-color` - Sandy orange (#f4a460)

## Preview

Open any HTML file directly in a browser - no server required.
