# WordPress Elementor Setup Instructions

## Files in this folder

| File | Description |
|------|-------------|
| `extract-all-pages.html` | **Main file** - Open this in a browser to extract all page HTML |
| `styles.css` | All CSS styles from the original website |
| `00-instructions.md` | This file |

## How to Use

### Step 1: Add Google Fonts to WordPress
Add these Google Fonts to your WordPress site (via Elementor > Site Settings > Custom CSS, or a plugin like "Asset CleanUp" or "Insert Headers and Footers"):

```html
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;500;600;700&family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@500;700&display=swap" rel="stylesheet">
```

### Step 2: Add Global CSS
Copy the contents of `styles.css` and paste it into:
- **Elementor Pro**: Elementor > Site Settings > Custom CSS
- **Without Elementor Pro**: Use a plugin like "Simple Custom CSS" or add to your theme's custom CSS

### Step 3: Extract Each Page's HTML

1. Open `extract-all-pages.html` in your web browser (Chrome, Firefox, Edge)
2. The page will show all 16 pages with their complete HTML code
3. Click the **"Copy HTML"** button for the page you want
4. In WordPress, create a new page with Elementor
5. Add a **"Custom HTML"** widget (or "Raw HTML" widget)
6. Paste the copied HTML code
7. Publish/Update the page

### Step 4: Repeat for Each Page

The 16 pages available:

| # | Page Name | WordPress Page |
|---|-----------|----------------|
| 1 | Home | Homepage |
| 2 | Water Damage Restoration | /water-damage/ |
| 3 | Fire & Smoke Damage Restoration | /fire-damage/ |
| 4 | Mold Remediation Coordination | /mold-remediation/ |
| 5 | Storm Damage Repairs | /storm-damage/ |
| 6 | Contents Pack-Out & Storage | /pack-out-storage/ |
| 7 | Complete Reconstruction | /reconstruction/ |
| 8 | Insurance Information | /insurance/ |
| 9 | Our Process | /our-process/ |
| 10 | About Us | /about/ |
| 11 | Service Areas | /service-areas/ |
| 12 | FAQ | /faq/ |
| 13 | Project Gallery | /gallery/ |
| 14 | Contact | /contact/ |
| 15 | Privacy Policy | /privacy/ |
| 16 | Terms of Service | /terms/ |

### Notes
- Each page's HTML includes the header, navigation, footer, all styles, and embedded images
- Images are base64-encoded (embedded directly in the HTML), so no external image files are needed
- For production, you may want to upload images to WordPress Media Library and update the `src` attributes
- The navigation links use `data-nav` attributes for the SPA behavior - in WordPress these will need to link to actual page URLs
- Mobile menu and sticky CTA are included in each page
