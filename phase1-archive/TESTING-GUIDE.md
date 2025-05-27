# Quick Testing Guide - Start Here!

## 🚀 Ready to Test? Follow These Steps:

### Step 1: Open Your Moodle Test Page
1. Go to your Lab's Moodle site
2. Navigate to your test page
3. Click "Edit" or "Turn editing on"
4. Edit the page content

### Step 2: Try Your First Test
1. In the Moodle editor, click the **HTML source** button (`<>` or "HTML" button)
2. Copy this simple test code:

```html
<div style="color: red; font-size: 20px;">🔴 RED TEXT TEST - If you see this in red, basic styling works!</div>
```

3. Paste it into the HTML editor
4. Click "Save" or "Update"
5. View the page

### Step 3: Document What Happened
**What you should see:**
- ✅ **Success**: Red text appears → Moodle allows basic inline CSS
- ❌ **Failure**: Text appears but not red → Moodle strips color styling
- 🚫 **Error**: Page won't save or shows error → Moodle blocks the code

**Record it in:** `results/test-log.md` (update the H002 row)

### Step 4: Try More Tests
**Next easy tests to try:**
1. **Basic div** (from `test-snippets/html-tests/basic-elements.html`)
2. **JavaScript button** (from `test-snippets/js-tests/javascript-tests.html`)

### Step 5: Take Screenshots
- Save screenshots of successful tests in `results/screenshots/`
- Name them like: `test-H002-red-text.png`

## 📁 Where to Find Test Code
- **HTML tests**: `test-snippets/html-tests/basic-elements.html`
- **CSS tests**: `test-snippets/css-tests/styling-tests.html`
- **JavaScript tests**: `test-snippets/js-tests/javascript-tests.html`

## 📝 Where to Document Results
- **Main log**: `results/test-log.md`
- **Screenshots**: `results/screenshots/`

## ❓ Need Help?
If something doesn't work as expected or you get stuck, that's valuable data! Document it and ask for help.

---

**🎯 Your Goal**: Start with the red text test above, then work through the other test snippets one by one! 