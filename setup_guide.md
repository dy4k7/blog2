# Website Structure Setup Guide

## 📁 File Structure

```
your-website/
├── index.html                  # Home page
├── shared-styles.css          # Shared styles for all pages
├── daily-logs.html            # Daily logs index page
├── 2025-11-10.html           # Individual daily log
├── 2025-11-09.html           # Individual daily log
├── 2025-11-08.html           # Individual daily log
└── ...more daily logs
```

## 🚀 Quick Start

### 1. Create the shared styles file
Save the `shared-styles.css` file in your root directory. This contains all the common styles (fonts, navigation, background, animations) that every page will use.

### 2. Update your home page
Replace your current `index.html` with the updated version that includes the "Daily Logs" link in the navigation.

### 3. Create the daily logs index
Save `daily-logs.html` in your root directory. This is the page that lists all your daily entries.

### 4. Create individual daily log pages
For each day, create a new HTML file named with the date format: `YYYY-MM-DD.html` (e.g., `2025-11-10.html`)

## ✍️ Adding a New Daily Log

### Method 1: Copy Template
1. Copy the `daily-log-template.html`
2. Rename it to today's date (e.g., `2025-11-11.html`)
3. Update the content:
   - Change the date in `<title>` and `<h1>`
   - Update the stats (hours studied, topics covered, etc.)
   - Add your log entries
   - Update "Previous Day" and "Next Day" links

### Method 2: Quick Daily Log Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Daily Log - [DATE] | Dhayalan K</title>
    <link rel="stylesheet" href="shared-styles.css">
    <link rel="stylesheet" href="daily-log-styles.css"> <!-- If you want specific log styles -->
</head>
<body>
    <!-- Copy the noise, floating-shapes, and nav from template -->
    
    <div class="container">
        <div class="page-header">
            <h1>[Your Date]</h1>
            <p>Daily Learning Journey</p>
        </div>
        
        <!-- Your content here -->
    </div>
</body>
</html>
```

## 🎨 Maintaining Consistent Theme

### All pages automatically share:
✅ **Fonts**: Playfair Display (headings) & Space Grotesk (body)
✅ **Colors**: Purple gradient theme (#8b5cf6, #a78bfa, #c4b5fd)
✅ **Background**: Animated gradient with noise texture
✅ **Navigation**: Fixed top navigation with auto-hide on scroll
✅ **Animations**: Fade-ins, hover effects, floating shapes
✅ **Layout**: Same container width, padding, spacing

### To customize a specific page:
Add a `<style>` block AFTER the shared-styles link:
```html
<link rel="stylesheet" href="shared-styles.css">
<style>
    /* Your page-specific styles here */
    .custom-element {
        /* ... */
    }
</style>
```

## 📝 Updating the Daily Logs Index

When you add a new daily log, update `daily-logs.html`:

1. Find the `<div class="log-list">` section
2. Add a new entry at the top:
```html
<a href="2025-11-11.html" class="log-card">
    <div class="log-date">[Your Date]</div>
    <div class="log-summary">
        [Brief summary of what you learned]
    </div>
    <div class="log-meta">
        <span>📚 [X] Topics</span>
        <span>⏱️ [X] Hours</span>
        <span>🏷️ [Tags]</span>
    </div>
</a>
```

## 🔗 Navigation Links Explained

### Home Page (index.html)
- Links to `#about`, `#focus`, `#contact` (sections on same page)
- Links to `daily-logs.html` (separate page)

### Daily Log Pages
- Link to `index.html` (home)
- Link to `daily-logs.html` (all logs)
- Link to previous/next day logs

### Daily Logs Index
- Links to `index.html` (home)
- Links to individual daily log files

## 💡 Pro Tips

1. **Naming Convention**: Stick to `YYYY-MM-DD.html` format for easy sorting
2. **Regular Updates**: Update the daily-logs.html index when you add new entries
3. **Consistency**: Use the same structure in all daily logs for a professional look
4. **Navigation**: Always test that all links work after adding new pages
5. **Mobile**: The design is responsive, but test on mobile devices

## 🎯 Example Workflow

**Every day:**
1. Copy yesterday's log file
2. Rename it to today's date
3. Update the content with today's learning
4. Update previous/next navigation links
5. Add an entry in `daily-logs.html`
6. Commit to GitHub (if using version control)

## 🚨 Common Issues

**Styles not loading?**
- Check that `shared-styles.css` is in the same directory as your HTML files
- Verify the `<link>` tag path is correct

**Navigation not working?**
- Ensure all href links point to existing files
- Check for typos in filenames

**Fonts not showing?**
- The fonts are loaded from Google Fonts in shared-styles.css
- Requires internet connection to load

## 📱 Testing Checklist

Before publishing:
- ✅ All navigation links work
- ✅ Styles load correctly on all pages
- ✅ Pages look good on desktop and mobile
- ✅ Previous/Next day links are correct
- ✅ Daily logs index is up to date