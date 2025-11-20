# Performance Report Creation Guide
## Daisy MD Care Template Base

**Purpose:** Document the standard process for creating consumer account performance reports using the Daisy MD Care HTML template as the base.

**Created:** November 19, 2025
**Template Version:** 2.0 (Refined Design + Mobile Optimized)
**Status:** ✅ Production Ready

---

## 🎯 Quick Start

When asked to create a performance report for a consumer account:

1. **Use Daisy MD Care as the base template**
2. **Replace account-specific data** (campaign names, metrics, etc.)
3. **Maintain the design system** (colors, spacing, typography)
4. **Deploy to GitHub & Vercel**

---

## 📋 Account-Specific Template Information

### Current Template: Daisy MD Care (Consumer Account)

**Files:**
- Desktop/Responsive: `index.html` (40KB)
- Mobile Optimized: `mobile.html` (29KB)
- Design Docs: `DESIGN_IMPROVEMENTS.md`

**Repository:** `https://github.com/gattari86/DaisyPerformance`

**Key Specifications:**
- Teal/dark blue color scheme (#0a3d4d, #5bb3c4)
- Light teal accents (#ffc107 for highlights)
- Professional typography hierarchy (h1-h4)
- Standardized spacing system (8-56px)
- Responsive design (5 breakpoints)
- Dark mode & accessibility support

---

## 🔄 Process for Creating New Consumer Account Reports

### Step 1: Prepare Data

**Gather from client:**
- Campaign names and performance dates
- Key metrics (impressions, clicks, conversions, CTR, CPC, etc.)
- Campaign status (active/archived)
- Performance rankings by metric
- Key takeaways and insights

**Organize data into categories:**
- Executive Summary (key metrics)
- Campaign Breakdown (individual campaign performance)
- Rankings (best performing keywords, campaigns)
- Key Takeaways (positive results, learnings)

### Step 2: Copy Base Template

```bash
# Clone the DaisyPerformance repository
git clone https://github.com/gattari86/DaisyPerformance.git [AccountName]Performance
cd [AccountName]Performance

# Or create new repo from template
# Files to copy:
#   - index.html (desktop version)
#   - mobile.html (mobile version)
#   - DESIGN_IMPROVEMENTS.md (documentation)
#   - vercel.json (deployment config)
```

### Step 3: Update HTML Content

**In `index.html` (and `mobile.html`):**

#### Header Section
```html
<header>
    <h1>[ACCOUNT NAME] - Campaign Performance Report</h1>
    <div class="header-tagline">Performance Analysis & Key Insights</div>
    <div class="header-report-title">
        <strong>Report Period:</strong> [DATE RANGE] | <strong>Generated:</strong> [DATE]
    </div>
</header>
```

#### Executive Summary - Metric Cards
Replace with account-specific KPIs:
```html
<div class="metric-card">
    <div class="metric-label">[METRIC NAME]</div>
    <div class="metric-value">[VALUE]</div>
</div>
```

**Common Metrics for Consumer Accounts:**
- Total Impressions
- Total Clicks
- Total Conversions
- Average CTR (Click-Through Rate)
- Average CPC (Cost Per Click)
- Conversion Rate
- Total Spend

#### Campaign Cards
Replace campaign names and data:
```html
<div class="campaign-card">
    <div class="campaign-header">
        <div class="campaign-icon">[ICON]</div>
        <div class="campaign-header-content">
            <h3>[CAMPAIGN NAME]</h3>
            <span class="campaign-status [active/archived]">[STATUS]</span>
        </div>
    </div>
    <!-- Campaign metrics table -->
    <table class="metrics-table">
        <thead>
            <tr>
                <th>Metric</th>
                <th>Value</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Impressions</td>
                <td>[VALUE]</td>
            </tr>
            <!-- More rows... -->
        </tbody>
    </table>
</div>
```

**Important:** Only one campaign should have `class="campaign-card top-performer"` for visual distinction (highest performer).

#### Ranking Sections
Replace with account-specific rankings:
```html
<div class="ranking-card">
    <h4>[CATEGORY - e.g., TOP PERFORMING KEYWORDS]</h4>
    <div class="ranking-items">
        <div class="ranking-item">
            <span class="ranking-rank">1</span>
            <span class="ranking-name">[KEYWORD/ITEM]</span>
            <span class="ranking-value">[METRIC]</span>
        </div>
        <!-- More items... -->
    </div>
</div>
```

#### Key Takeaways
Replace with account-specific insights:
```html
<div class="takeaway-item positive">
    <h4>✅ [Positive Result Title]</h4>
    <p>[Description of what worked well]</p>
</div>

<div class="takeaway-item info">
    <h4>ℹ️ [Learning or Insight]</h4>
    <p>[Description of key learning]</p>
</div>

<div class="takeaway-item positive">
    <h4>✅ [Another Success]</h4>
    <p>[Description of success]</p>
</div>
```

#### Footer
Update metadata:
```html
<footer>
    <div class="footer-divider"></div>
    <p><strong>Account:</strong> [ACCOUNT NAME]</p>
    <p><strong>Report Period:</strong> [DATE RANGE]</p>
    <p><strong>Generated:</strong> [DATE]</p>
    <p><strong>Report Version:</strong> [VERSION]</p>
</footer>
```

### Step 4: Verify Styling

**Maintain Design Consistency:**
- ✅ Use existing color palette (no custom colors)
- ✅ Keep typography hierarchy (h1-h4)
- ✅ Maintain spacing system (8-56px increments)
- ✅ Don't modify CSS unless necessary
- ✅ Use provided badge/status classes only

**Color Reference:**
```css
Primary Teal:       #0a3d4d (headings, primary text)
Secondary Teal:     #5bb3c4 (borders, accents)
Gold:               #ffc107 (top performer highlights)
Accent Blue:        #2196f3 (info sections)
Accent Green:       #4caf50 (positive items)
Danger Red:         #d32f2f (critical metrics)
Light Gray:         #f5f7fa (backgrounds)
Text:               #2c3e50 (body text)
```

### Step 5: Create Repository

```bash
# Initialize git repo (if new)
git init
git add .
git commit -m "Initial campaign performance report for [ACCOUNT NAME]"
git remote add origin https://github.com/gattari86/[AccountName]Performance.git
git push -u origin main
```

### Step 6: Deploy to Vercel

1. Go to https://vercel.com
2. Click "New Project"
3. Select GitHub repository
4. Vercel auto-detects configuration
5. Click "Deploy"
6. Get live HTTPS URL

---

## 📊 Data Mapping Reference

### Standard Metrics to Include

**Campaign Performance:**
| Metric | Definition | Example |
|--------|-----------|---------|
| Impressions | Number of times ads shown | 45,293 |
| Clicks | Number of clicks on ads | 1,324 |
| CTR | Click-Through Rate | 2.92% |
| CPC | Cost Per Click | $3.12 |
| Conversions | Completed actions | 8 |
| Conversion Rate | % of clicks that converted | 0.60% |
| ROAS | Return on Ad Spend | 2.4x |

**Ranking Categories:**
- Top Performing Keywords (by CTR, conversions, etc.)
- Best Performing Campaigns
- Highest Converting Keywords
- Most Expensive Keywords
- Best ROI Keywords

### Naming Conventions

**Campaign Names:**
- Geographic focus: "[Location] Campaign" (e.g., "Van Nuys Campaign")
- Service focus: "[Service] Campaign" (e.g., "Skincare Campaign")
- Combined: "[Service] - [Location]" (e.g., "Acne Treatment - Houston")

**Status Values:**
- `active` - Currently running
- `archived` - Previously completed
- `paused` - Temporarily stopped

---

## 🎨 Design Customization (Optional)

### If Custom Styling Needed:

**DO NOT modify:**
- Color palette (#0a3d4d, #5bb3c4, #ffc107)
- Typography system (h1-h4 sizes)
- Spacing increments (8px base)

**SAFE to customize:**
- Account name and branding
- Report title and tagline
- Campaign names and icons
- Metric values and labels
- Takeaway text and descriptions

### Adding New Sections (Advanced)

If you need to add new sections beyond the template:

1. **Create new `<section>` with class name**
2. **Use existing CSS structure:**
   ```css
   .new-section {
       background: white;
       border-radius: 16px;
       padding: 40px;
       margin-bottom: 32px;
       box-shadow: 0 8px 16px rgba(0, 0, 0, 0.12);
   }
   ```
3. **Follow spacing system** (multiples of 8px)
4. **Keep color palette consistent**
5. **Test at all breakpoints** (mobile, tablet, desktop)

---

## 🚀 Complete Checklist

- [ ] **Data gathered** from client
- [ ] **Header updated** with account name and dates
- [ ] **Executive summary** metrics entered
- [ ] **Campaign cards** populated with data
- [ ] **Ranking sections** filled with rankings
- [ ] **Key takeaways** written with insights
- [ ] **Footer** updated with metadata
- [ ] **Mobile version** updated with same data
- [ ] **All links verified** (if any)
- [ ] **CSS not modified** (uses base template)
- [ ] **Color scheme** matches template
- [ ] **Responsive design** tested (mobile, tablet, desktop)
- [ ] **Dark mode** tested
- [ ] **Accessibility** verified (headings, contrast)
- [ ] **Performance** checked (page load < 1s)
- [ ] **GitHub repository** created
- [ ] **Vercel deployed** and live
- [ ] **Documentation** created/updated

---

## 📚 File Structure for New Reports

```
[AccountName]Performance/
├── index.html                    # Desktop/responsive version
├── mobile.html                   # Mobile-optimized version
├── README.md                     # Project overview
├── DESIGN_IMPROVEMENTS.md        # Design documentation
├── REPORT_CREATION_GUIDE.md      # This guide
├── vercel.json                   # Vercel deployment config
├── package.json                  # Project metadata
├── .gitignore                    # Git ignore rules
└── .git/                         # Git repository
```

---

## 🔗 Template Resources

**Base Template (Daisy MD Care):**
- Repository: https://github.com/gattari86/DaisyPerformance
- Desktop Version: `index.html`
- Mobile Version: `mobile.html`
- Design Docs: `DESIGN_IMPROVEMENTS.md`

**Copy These Files For New Reports:**
1. `index.html` - Update with new account data
2. `mobile.html` - Update with same account data
3. `vercel.json` - Use as-is for deployment
4. `package.json` - Update project name only
5. `.gitignore` - Use as-is

---

## 💡 Pro Tips

### Data Entry Best Practices

1. **Use consistent number formatting:**
   - Large numbers: 45,293 (use commas)
   - Percentages: 2.92% (always 2 decimals)
   - Currency: $3.12 (use $ sign)

2. **Write clear takeaways:**
   - Be specific (cite metrics)
   - Be actionable (what to do next)
   - Be concise (2-3 sentences max)

3. **Choose representative icons:**
   - 📍 Geographic campaigns
   - 🏢 Service campaigns
   - 📊 Data/metric campaigns
   - 🎯 Targeting campaigns

4. **Rank logically:**
   - Top rankings by performance metric
   - Show 3-5 items per category
   - Include both successes and learnings

### Performance Optimization

- Keep HTML file < 50KB
- Minimize image usage
- Use system fonts (no web fonts)
- Test on real devices
- Verify Core Web Vitals

### Accessibility

- Maintain heading hierarchy (h1 > h2 > h3)
- Use semantic HTML
- Ensure color contrast ratios (WCAG AA)
- Support dark mode
- Respect reduced-motion preferences

---

## 🆘 Troubleshooting

### Report not displaying correctly?

1. **Check HTML syntax** - Validate at validator.w3.org
2. **Verify CSS** - Don't modify color hex values
3. **Test responsiveness** - Use browser dev tools
4. **Check file encoding** - Should be UTF-8

### Vercel deployment issues?

1. **Verify vercel.json** - Should be in root directory
2. **Check branch name** - Usually `main` not `master`
3. **Review error logs** - Check Vercel dashboard
4. **Test locally first** - Open HTML in browser

### Data not showing?

1. **Check table syntax** - All `<tr>` tags closed
2. **Verify metric values** - No extra spaces/characters
3. **Review campaign names** - Match exactly
4. **Validate numbers** - Remove non-numeric characters

---

## 📝 Documentation to Create

For each new consumer account report, create:

1. **README.md** - Overview of the report
2. **REPORT_CREATION_GUIDE.md** - This guide (can be copied/customized)
3. **DESIGN_IMPROVEMENTS.md** - Design specifications (can be reused from template)

---

## ✅ Status

**Template Ready:** ✅ Yes
**Base System:** ✅ Daisy MD Care (index.html + mobile.html)
**Documentation:** ✅ Complete
**Deployment:** ✅ GitHub + Vercel Ready
**Quality:** ✅ Production Grade

---

**Next Step:** When you need a performance report for a consumer account, reference this guide to use the Daisy MD Care template as the base, update the data, and deploy!

