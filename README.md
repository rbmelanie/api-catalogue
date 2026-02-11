# Core Humanitarian Datasets Catalogue - Setup Instructions

## Overview
This prototype creates a searchable, filterable catalogue of humanitarian datasets with domain definitions. It's designed to be hosted on GitHub Pages for easy sharing with partners while remaining unlisted from search engines.

## What's Included

### Files in this package:
1. **index.html** - Main catalogue page with filtering and search
2. **domains.html** - Domain definitions page
3. **datasets.csv** - Your dataset data (currently has 5 sample entries)
4. **datasets-template.csv** - Empty template for adding datasets
5. **domains.csv** - Domain definitions (currently has 6 sample domains)
6. **domains-template.csv** - Empty template for adding domains
7. **README.md** - This file

## Quick Start Guide

### Step 1: Create a GitHub Account (if you don't have one)
1. Go to https://github.com
2. Click "Sign up"
3. Follow the registration process

### Step 2: Create a New Repository
1. Click the "+" icon in the top right → "New repository"
2. Repository name: `humanitarian-datasets-catalogue` (or any name you prefer)
3. **Important**: Select "Private" if you want only people with the link to access it
   - OR select "Public" but the unlisted link won't be indexed by search engines anyway
4. Check "Add a README file"
5. Click "Create repository"

### Step 3: Upload Your Files
1. In your new repository, click "Add file" → "Upload files"
2. Drag and drop ALL the files from this package:
   - index.html
   - domains.html
   - datasets.csv
   - domains.csv
   - (You can skip the template files, they're just for reference)
3. Add a commit message: "Initial catalogue setup"
4. Click "Commit changes"

### Step 4: Enable GitHub Pages
1. In your repository, click "Settings" (top menu)
2. Scroll down and click "Pages" in the left sidebar
3. Under "Source", select "main" branch
4. Click "Save"
5. Wait 1-2 minutes for deployment
6. A URL will appear at the top: `https://yourusername.github.io/humanitarian-datasets-catalogue/`

### Step 5: Access Your Catalogue
Your catalogue is now live at:
- **Main catalogue**: `https://yourusername.github.io/humanitarian-datasets-catalogue/`
- **Domain definitions**: `https://yourusername.github.io/humanitarian-datasets-catalogue/domains.html`

Share this link with your partners. It won't appear in search engines.

## How to Update Your Data

### Option A: Edit Directly on GitHub (Easiest)
1. Go to your repository on GitHub
2. Click on `datasets.csv`
3. Click the pencil icon (Edit this file)
4. Make your changes (add rows, modify data)
5. Scroll down, add a commit message: "Updated datasets"
6. Click "Commit changes"
7. Your website updates automatically in ~1 minute!

### Option B: Edit in Excel/Google Sheets
1. Download `datasets.csv` from your repository
2. Open in Excel or Google Sheets
3. Edit the data (add rows, update information)
4. Save as CSV
5. Go to GitHub → "Add file" → "Upload files"
6. Upload your updated `datasets.csv`
7. Commit changes

## CSV File Structure

### datasets.csv Columns:
All fields are included. You can leave fields empty if not applicable.

| Column Name | Description | Required |
|------------|-------------|----------|
| Owner / Lead | Organization responsible | Yes |
| Domain | Category (Health, Food Security, etc.) | Yes |
| Dataset Name | Name of the dataset | Yes |
| Description | What the dataset contains | Yes |
| Sources | Where the data comes from | No |
| Data collection frequency / ingestion | How often data is collected | No |
| Data Publication frequency | How often data is published | No |
| Disaggregation | How data is broken down (age, sex, etc.) | No |
| Countries | Countries covered (separate with semicolons) | No |
| Geographical disaggregation | Admin level (Admin 0, Admin 1, etc.) | No |
| Data dictionary / Schema | Link to schema documentation | No |
| API or main ingestion source | Link to API or data source | No |
| HDX Link | Link to HDX page | No |
| License | Data license (CC BY, Public Domain, etc.) | No |
| Other technical considerations | Additional notes | No |

### domains.csv Columns:
| Column Name | Description |
|------------|-------------|
| Domain | Domain name (must match domains in datasets.csv) |
| Definition | What this domain covers |
| Exclusions | What is NOT included in this domain |
| Primary Question Answered | Key question this domain addresses |

## Important CSV Tips

### Handling Commas in Text
If your text contains commas, wrap it in quotes:
```csv
UNICEF,Health,"Data includes coverage rates, vaccination schedules, and more",Data source
```

### Multi-Country Format
Separate multiple countries with semicolons:
```csv
Countries
"Syria; Lebanon; Jordan; Turkey"
```

### Line Breaks in Descriptions
For longer descriptions, keep them on one line or use quotes:
```csv
Description
"This dataset provides comprehensive information about refugee populations across multiple countries and includes detailed demographic breakdowns."
```

## Customization Options

### Change Colors
Edit the CSS variables in `index.html` and `domains.html` (around line 16-25):
```css
:root {
    --primary-green: #1ebfb3;    /* Change this to your brand color */
    --dark-green: #138f85;       /* Darker shade of your color */
    /* ... other colors ... */
}
```

### Add Your Logo
In the header section of both HTML files, you can add:
```html
<img src="your-logo.png" alt="Logo" style="height: 50px;">
```

### Change Text/Titles
All text is directly in the HTML files - search for the text and replace it.

## Privacy & Security

### Keeping It Private
- Use a **Private repository** if you only want people with the link to access it
- Even with a Public repository, the link is not indexed by search engines (meta robots tag is set)
- Share only the direct link with partners
- Don't link to it from public websites

### No Search Engine Indexing
Both pages include:
```html
<meta name="robots" content="noindex, nofollow">
```
This prevents search engines from indexing your catalogue.

## Troubleshooting

### Problem: Website not loading
- Wait 2-3 minutes after enabling GitHub Pages
- Check that GitHub Pages is enabled in Settings → Pages
- Verify your files are in the main branch

### Problem: Data not showing
- Check that `datasets.csv` is in the root of your repository
- Open the browser console (F12) to see error messages
- Verify your CSV has proper formatting (no extra commas)

### Problem: Filters not working
- Make sure domain names in `datasets.csv` exactly match those in `domains.csv`
- Check for extra spaces or special characters

### Problem: CSV formatting errors
- Use quotes around fields with commas
- Ensure each row has the same number of columns
- Don't use line breaks within fields (or wrap in quotes if needed)

## Handover to Development Team

When you're ready to hand this over to your development team, they'll have:

1. **Clean HTML/CSS/JavaScript** - All code is well-structured and commented
2. **Complete Git history** - All changes tracked in GitHub
3. **Structured data in CSV** - Easy to migrate to a database
4. **Responsive design** - Works on mobile, tablet, and desktop

### What They Can Do:
- Migrate CSV to a database (PostgreSQL, MySQL, etc.)
- Add user authentication
- Implement backend API
- Add advanced features (export, charts, etc.)
- Integrate with your main website
- Add automated data updates

### Repository Access:
- Add them as collaborators: Settings → Collaborators → Add people
- Or transfer ownership: Settings → Transfer repository

## Next Steps

1. ✅ Upload files to GitHub
2. ✅ Enable GitHub Pages
3. ✅ Replace sample data with your actual datasets
4. ✅ Add your domain definitions
5. ✅ Share the link with partners
6. ✅ Gather feedback
7. ✅ Iterate and improve

## Support

For questions or issues:
- Check the troubleshooting section above
- Review GitHub Pages documentation: https://docs.github.com/en/pages
- Contact your technical team for assistance

## Future Enhancements (Optional)

Consider these additions when handing over to your dev team:
- Export to Excel/PDF functionality
- Advanced filtering (multiple domains, date ranges)
- Dataset comparison tool
- Automated data validation
- RSS feed for new datasets
- Email notifications for updates
- Integration with your existing systems
- Analytics tracking (who's using which datasets)

---

**Version**: 1.0  
**Last Updated**: February 2026  
**Created for**: Humanitarian Data Teams
