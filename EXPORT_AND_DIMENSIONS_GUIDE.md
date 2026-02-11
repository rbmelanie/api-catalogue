# Export & Dimensions Feature Guide

## ✅ Export Feature - NOW AVAILABLE!

### How It Works

Users can now export their **filtered results** in two formats:

#### 1. **Export CSV Button** (⬇️ Export CSV)
- Downloads current filtered view as CSV file
- Filename: `humanitarian_datasets_YYYY-MM-DD.csv`
- Opens in Excel, Google Sheets, or any spreadsheet software
- Perfect for data analysis

#### 2. **Export Excel Button** (⬇️ Export Excel)
- Downloads current filtered view as Excel file (.xls)
- Filename: `humanitarian_datasets_YYYY-MM-DD.xls`
- Pre-formatted with HDX green header
- Opens directly in Microsoft Excel

### Use Cases

**Scenario 1: Domain-Specific Export**
1. Filter by Domain = "Population"
2. Click "Export CSV"
3. Get only Population datasets

**Scenario 2: Organization Report**
1. Filter by Organization = "OCHA"
2. Filter by Frequency = "Annually"
3. Click "Export Excel"
4. Share with team

**Scenario 3: Custom Selection**
1. Use multi-select to choose 5 specific datasets
2. Click "Export CSV"
3. Compare just those 5

**Scenario 4: Complete Catalog**
1. No filters applied (shows all)
2. Click "Export Excel"
3. Full catalog backup

### Technical Details

- **Pure client-side** - No server needed
- Works in all modern browsers
- Properly escapes commas, quotes, newlines
- Includes all metadata fields
- Respects current sort order

---

## 🏷️ Dimensions Feature - READY FOR DATA!

### What Are Dimensions?

Dimensions are **flexible tags** that go beyond domains. They describe characteristics like:

- **Temporal**: real-time, historical, forecasted
- **Quality**: validated, peer-reviewed, preliminary
- **Access**: public, restricted, on-request
- **Coverage**: comprehensive, sample-based
- **Status**: active, archived, beta
- **Type**: geospatial, timeseries, cross-sectional

### How to Add Dimensions Data

#### Option 1: Edit CSV Directly

The CSV already has a "Dimensions" column (last column). Add tags separated by semicolons:

```csv
Dataset Name,Owner / Lead,...,Dimensions
IDP Baseline,IOM,...,"real-time; validated; public"
Food Prices,WFP,...,"real-time; comprehensive"
Population Stats,UNHCR,...,"quarterly; validated"
```

#### Option 2: Edit Excel

1. Open `datasets_cleaned.xlsx`
2. Add values to "Dimensions" column (last column)
3. Use semicolons to separate multiple dimensions
4. Save as CSV with exact name: `datasets.csv`

### Example Dimensions by Domain

**Population Data:**
- real-time, quarterly, validated, public, comprehensive

**Food Security:**
- real-time, market-based, daily-updates, public

**Coordination:**
- quarterly, validated, restricted, operational

**Geographic:**
- reference, validated, public, authoritative

### Filter Behavior

Once dimensions data is added:
1. **Filter automatically appears** - No code changes needed!
2. **Dropdown populated** - All unique dimensions listed
3. **Multi-match support** - Filters datasets with ANY matching dimension

### Recommended Dimension Vocabulary

Consider standardizing on these common dimensions:

**Temporal Dimensions:**
- `real-time` - Updated continuously or daily
- `near-real-time` - Updated within 48 hours
- `periodic` - Regular scheduled updates
- `snapshot` - Point-in-time data
- `historical` - Archive/past data
- `forecasted` - Predictive/future data

**Quality Dimensions:**
- `validated` - Verified by authoritative source
- `peer-reviewed` - External validation
- `preliminary` - Initial/unverified data
- `estimated` - Modeled/inferred values
- `self-reported` - Direct from source without validation

**Access Dimensions:**
- `public` - Openly accessible
- `restricted` - Access requires permission
- `on-request` - Available upon application
- `internal` - Organization-only

**Coverage Dimensions:**
- `comprehensive` - Complete coverage
- `sample-based` - Representative sample
- `partial` - Incomplete coverage
- `pilot` - Limited geographic scope

**Status Dimensions:**
- `active` - Currently maintained
- `beta` - Testing phase
- `archived` - No longer updated
- `deprecated` - Replaced by newer dataset

**Type Dimensions:**
- `geospatial` - Location-based
- `timeseries` - Temporal sequence
- `cross-sectional` - Snapshot across entities
- `panel` - Same entities over time

### Implementation Examples

#### Example 1: Real-time Crisis Data
```csv
Emergency Event Tracking,IOM,...,"real-time; validated; public; geospatial"
```

#### Example 2: Annual Reports
```csv
Humanitarian Response Plans,OCHA,...,"annual; validated; public; comprehensive"
```

#### Example 3: Beta Dataset
```csv
AI Risk Predictions,Centre,...,"forecasted; beta; restricted; experimental"
```

### Advanced: Dimension Hierarchies

You could organize dimensions hierarchically:

```csv
Dimensions
"temporal:real-time; quality:validated; access:public"
```

This allows for more sophisticated filtering in future versions.

---

## 🎯 Benefits

### Export Benefits:
- ✅ Share filtered data with stakeholders
- ✅ Offline analysis in Excel
- ✅ Integration with other tools
- ✅ Backup/archiving
- ✅ Custom reports

### Dimensions Benefits:
- ✅ More precise filtering
- ✅ Multi-faceted categorization
- ✅ Better discovery
- ✅ Quality indicators
- ✅ Access management clarity

---

## 📝 Quick Start Checklist

### To Use Export (Available Now):
- [x] Filter datasets as desired
- [x] Click "Export CSV" or "Export Excel"
- [x] File downloads automatically
- [x] Open in your preferred tool

### To Enable Dimensions:
- [ ] Decide on dimension vocabulary (see recommendations above)
- [ ] Add dimensions to datasets.csv (last column)
- [ ] Use semicolons to separate multiple dimensions
- [ ] Upload updated datasets.csv
- [ ] Filter appears automatically! ✨

---

## 🔧 Troubleshooting

**Export Not Working?**
- Check browser allows downloads
- Disable popup blockers
- Try different browser
- Check console for errors (F12)

**Dimensions Not Appearing?**
- Verify "Dimensions" column has data
- Check for typos in column header
- Ensure semicolon separation
- Refresh page after uploading new CSV

**Excel Export Opens in Browser?**
- Right-click → "Save As"
- Or change browser download settings

---

## 💡 Future Enhancement Ideas

### Export Enhancements:
1. **Export Options Dialog**
   - Choose which columns to include
   - Select format (CSV, Excel, JSON, PDF)
   - Include/exclude expanded metadata

2. **Scheduled Exports**
   - Auto-export weekly snapshots
   - Email distribution lists

3. **API Export**
   - Direct download via URL
   - Programmatic access

### Dimensions Enhancements:
1. **Dimension Badges**
   - Visual tags on cards/rows
   - Color-coded by type

2. **Multi-Select Dimensions Filter**
   - Filter by multiple dimensions at once
   - "AND" vs "OR" logic

3. **Dimension Statistics**
   - Show count of datasets per dimension
   - Dimension popularity chart

4. **Auto-Suggest Dimensions**
   - AI suggests dimensions based on description
   - Consistency checking

---

**Updated**: February 2026  
**Version**: 2.1 (Export + Dimensions Ready)
