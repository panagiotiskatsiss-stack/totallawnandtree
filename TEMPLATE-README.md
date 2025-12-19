# Tree Service Website Template

A complete, SEO-optimized website template for tree service businesses. Each HTML file is self-contained with embedded CSS - no build tools required.

---

## Quick Start for New Client

1. **Duplicate this folder** for each new client project
2. **Find & Replace** all placeholders (see table below)
3. **Add client logo** and update `{{LOGO_IMAGE}}` path
4. **Embed forms** from GoHighLevel/Lead Connector
5. **Add reviews widget** embed code
6. **Deploy** to hosting

---

## Placeholder Variables

Replace these across ALL HTML files:

### Business Info
| Placeholder | Description | Example |
|-------------|-------------|---------|
| `{{BUSINESS_NAME}}` | Company name | Total Lawn and Tree |
| `{{PHONE}}` | Business phone | (555) 123-4567 |
| `{{EMAIL}}` | Contact email | info@totallawnandtree.com |
| `{{ADDRESS}}` | Street address | 123 Main St |
| `{{CITY}}` | Primary city | Dallas |
| `{{STATE}}` | State abbreviation | TX |

### Service Areas (5 areas supported)
| Placeholder | Description | Example |
|-------------|-------------|---------|
| `{{AREA_1}}` | First service area name | Plano |
| `{{AREA_1_SLUG}}` | URL-friendly version | plano |
| `{{AREA_2}}` | Second service area | Frisco |
| `{{AREA_2_SLUG}}` | URL-friendly version | frisco |
| `{{AREA_3}}` | Third service area | McKinney |
| `{{AREA_3_SLUG}}` | URL-friendly version | mckinney |
| `{{AREA_4}}` | Fourth service area | Allen |
| `{{AREA_4_SLUG}}` | URL-friendly version | allen |
| `{{AREA_5}}` | Fifth service area | Richardson |
| `{{AREA_5_SLUG}}` | URL-friendly version | richardson |

### Assets & Embeds
| Placeholder | Description |
|-------------|-------------|
| `{{LOGO_IMAGE}}` | Path to logo image (e.g., `images/logo.png`) |
| `{{INLINE_FORM_EMBED}}` | GoHighLevel inline form embed code |
| `{{POPUP_FORM_EMBED}}` | GoHighLevel popup form embed code |
| `{{REVIEWS_WIDGET_EMBED}}` | Third-party reviews widget (Google/Facebook) |

---

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
│   ├── area-tree-services.html        # [AREA] all services landing
│   ├── area-tree-removal.html         # [AREA] tree removal
│   ├── area-tree-pruning.html         # [AREA] tree pruning
│   ├── area-stump-grinding.html       # [AREA] stump grinding
│   ├── area-land-clearing.html        # [AREA] land clearing
│   └── area-emergency-tree-service.html # [AREA] emergency
│
├── CLAUDE.md                     # Claude Code instructions
├── TEMPLATE-README.md            # This file
└── images/                       # Client images folder
```

---

## Creating Area-Specific Pages

For each service area, duplicate the templates and rename:

**Example for "Plano" area:**
```
templates/area-tree-services.html  →  plano-tree-services.html
templates/area-tree-removal.html   →  plano-tree-removal.html
templates/area-tree-pruning.html   →  plano-tree-pruning.html
templates/area-stump-grinding.html →  plano-stump-grinding.html
templates/area-land-clearing.html  →  plano-land-clearing.html
templates/area-emergency-tree-service.html → plano-emergency-tree-service.html
```

Then replace `{{AREA}}` with "Plano" and `{{AREA_SLUG}}` with "plano" in those files.

---

## CSS Customization

Colors are defined as CSS variables in `:root` at the top of each file:

```css
:root {
    --primary-color: #2d5a27;      /* Main green */
    --primary-dark: #1e3d1a;       /* Darker green */
    --secondary-color: #8b4513;    /* Brown */
    --accent-color: #f4a460;       /* Sandy orange (CTAs) */
    --emergency-color: #dc3545;    /* Red (emergency pages) */
}
```

To change the color scheme, update these variables in each file.

---

## Form Integration

### Inline Forms (embedded in page content)
Replace `{{INLINE_FORM_EMBED}}` with your GoHighLevel/Lead Connector embed code:
```html
<iframe src="https://api.leadconnectorhq.com/widget/form/YOUR_FORM_ID" ...></iframe>
```

### Popup Forms (triggered by buttons)
Replace `{{POPUP_FORM_EMBED}}` with your popup script:
```html
<script src="https://api.leadconnectorhq.com/js/form_embed.js"></script>
```

---

## Reviews Widget

Replace `{{REVIEWS_WIDGET_EMBED}}` with your chosen reviews widget:

**Recommended options:**
- EmbedSocial
- Elfsight
- Taggbox
- Trustmary

Example:
```html
<script src="https://widget.elfsight.com/platform.js" defer></script>
<div class="elfsight-app-xxxxx"></div>
```

---

## SEO Features Included

- Schema.org LocalBusiness/Service/FAQPage JSON-LD markup
- Open Graph meta tags
- Geo meta tags for local SEO
- Proper H1/H2/H3 heading hierarchy
- Internal linking between all service pages
- Location-specific keywords in titles, meta descriptions, and content

---

## Deployment Checklist

- [ ] All placeholders replaced
- [ ] Logo uploaded and path updated
- [ ] Forms embedded and tested
- [ ] Reviews widget added
- [ ] All area pages created (if using multiple areas)
- [ ] Schema markup validated (Google Rich Results Test)
- [ ] Mobile responsiveness tested
- [ ] All links working
- [ ] Contact info correct
- [ ] Favicon added

---

## Support

Template created for agency use. For modifications, use Claude Code with the CLAUDE.md instructions file.
