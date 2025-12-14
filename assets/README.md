# Assets for JOB-EZ Demo

This folder contains visual assets for the project README.

## Required Files

### 1. `demo.gif` - Bot Automation Demo
**How to create:**
1. Install a screen recorder (e.g., **Kap** for macOS, **ScreenToGif** for Windows)
2. Run the bot: `python3 main.py`
3. Record the screen showing:
   - Browser opening with LinkedIn
   - Bot navigating to a job
   - Clicking "Easy Apply"
   - Filling form fields automatically
   - Uploading resume
   - Clicking "Next" → "Review" → "Submit"
4. Save as `demo.gif` (max 10MB, 800px wide recommended)

**Recommended tools:**
- **macOS**: [Kap](https://getkap.co/) (free, converts to GIF)
- **Windows**: [ScreenToGif](https://www.screentogif.com/) (free)
- **Online**: [CloudConvert](https://cloudconvert.com/) to convert video to GIF

**Settings:**
- Resolution: 1280x720 or 800px wide
- Frame rate: 10-15 fps (keeps file size small)
- Duration: 15-30 seconds
- Focus on key steps (trim loading times)

---

### 2. `job_tracker_screenshot.png` - Excel Tracker Screenshot
**How to create:**
1. Open `data/job_tracker.xlsx` in Excel
2. Make sure you have some sample applications (run the bot if needed)
3. Take a clean screenshot showing:
   - Column headers (Company, Location, Resume Used, Status, etc.)
   - At least 5-10 rows of data
   - Different status types (Success, Failed, Skipped)
4. Save as `job_tracker_screenshot.png`

**Recommended:**
- Use macOS: `Cmd + Shift + 4` (crop to selection)
- Use Windows: `Snipping Tool` or `Win + Shift + S`
- Crop to show just the relevant data (no empty cells)
- Make sure text is readable at 800px wide

**Optional enhancements:**
- Add a subtle border or shadow for polish
- Ensure no personal data is visible
- Consider highlighting interesting rows

---

## Quick Commands

### Check file sizes:
```bash
ls -lh assets/
```

### Optimize GIF (if too large):
```bash
# Install gifsicle (macOS)
brew install gifsicle

# Optimize GIF
gifsicle -O3 --colors 128 demo.gif -o demo_optimized.gif
```

### Optimize PNG:
```bash
# Install pngquant (macOS)
brew install pngquant

# Optimize PNG
pngquant job_tracker_screenshot.png --output job_tracker_screenshot_optimized.png
```

---

## GitHub Upload

Once files are created:
```bash
# Add assets to git
git add assets/demo.gif assets/job_tracker_screenshot.png

# Commit
git commit -m "Add demo GIF and job tracker screenshot"

# Push
git push origin dev
```

---

## Preview

After uploading, check the README on GitHub to verify images display correctly:
- https://github.com/Mithurn/JOB-EZ

If images don't show, verify:
1. Files are in `assets/` folder
2. File names match exactly (case-sensitive)
3. Files are pushed to GitHub
4. GitHub has processed the images (may take a minute)
