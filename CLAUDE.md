# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML website template for tree service businesses. Each HTML file is self-contained with embedded CSS - no build tools, bundlers, or external dependencies required.

## Template Customization

All HTML files use placeholder variables that must be replaced for each client:

### Business Placeholders
| Placeholder | Description | Example |
|-------------|-------------|---------|
| `{{BUSINESS_NAME}}` | Company name | Total Lawn and Tree |
| `{{CITY}}` | Primary city | Dallas |
| `{{STATE}}` | State abbreviation | TX |
| `{{PHONE}}` | Business phone | (555) 123-4567 |
| `{{EMAIL}}` | Contact email | info@company.com |
| `{{ADDRESS}}` | Street address | 123 Main St |

### Service Area Placeholders
| Placeholder | Description |
|-------------|-------------|
| `{{AREA_1}}` - `{{AREA_5}}` | Service area names (e.g., Plano) |
| `{{AREA_1_SLUG}}` - `{{AREA_5_SLUG}}` | URL-friendly versions (e.g., plano) |
| `{{AREA}}` | Current area name (in template files) |
| `{{AREA_SLUG}}` | Current area slug (in template files) |

### Asset & Embed Placeholders
| Placeholder | Description |
|-------------|-------------|
| `{{LOGO_IMAGE}}` | Path to logo image file |
| `{{INLINE_FORM_EMBED}}` | GoHighLevel/Lead Connector inline form |
| `{{POPUP_FORM_EMBED}}` | GoHighLevel/Lead Connector popup form |
| `{{REVIEWS_WIDGET_EMBED}}` | Third-party reviews widget code |

## File Structure

```
/
├── index.html                    # Homepage
├── tree-removal.html             # Tree Removal service page
├── tree-pruning.html             # Tree Pruning service page
├── stump-grinding.html           # Stump Grinding service page
├── land-clearing.html            # Land Clearing service page
├── emergency-tree-service.html   # Emergency service page
│
├── templates/                    # Area-specific page templates
│   ├── area-tree-services.html
│   ├── area-tree-removal.html
│   ├── area-tree-pruning.html
│   ├── area-stump-grinding.html
│   ├── area-land-clearing.html
│   └── area-emergency-tree-service.html
│
├── CLAUDE.md                     # This file (Claude instructions)
├── TEMPLATE-README.md            # Full template documentation
└── images/                       # Client images folder
```

## Common Tasks

### Setting up for a new client
1. Duplicate entire folder with client name
2. Find & replace all business placeholders across all files
3. Add client logo and update `{{LOGO_IMAGE}}` paths
4. Create area-specific pages from templates
5. Add form embed codes
6. Add reviews widget

### Creating area-specific pages
For each service area (e.g., "Plano"):
1. Copy template file: `templates/area-tree-services.html` → `plano-tree-services.html`
2. Replace `{{AREA}}` with "Plano"
3. Replace `{{AREA_SLUG}}` with "plano"
4. Repeat for all 6 template types

### Changing colors
Update CSS variables in `:root` at top of each file's `<style>` block:
```css
--primary-color: #2d5a27;      /* Main green */
--primary-dark: #1e3d1a;       /* Darker green */
--secondary-color: #8b4513;    /* Brown */
--accent-color: #f4a460;       /* Sandy orange */
--emergency-color: #dc3545;    /* Red (emergency pages only) */
```

## SEO Features

Each page includes:
- Schema.org LocalBusiness/Service/FAQPage JSON-LD markup
- Open Graph meta tags
- Geo meta tags for local SEO
- Proper H1/H2/H3 heading hierarchy
- Internal linking between all service pages
- Location-specific keywords

## Navigation Structure

The header includes:
- Logo (image)
- Home, Tree Removal, Tree Pruning, Land Clearing, Stump Grinding, Emergency links
- Service Areas dropdown (hover on desktop, tap on mobile)
- CTA button (Free Estimate / Call Now)

## Preview

Open any HTML file directly in a browser - no server required.

## Important Notes

- When editing, apply changes to ALL 12 HTML files (6 main + 6 templates)
- Test responsive behavior at 1024px and 768px breakpoints
- Validate Schema markup with Google Rich Results Test after edits
