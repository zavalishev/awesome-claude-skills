---
name: playwright-automation
description: "Complete browser automation with Playwright. Auto-detects dev servers, writes test scripts to /tmp. Test pages, fill forms, take screenshots, check responsive design, validate UX, test login flows."
source: https://github.com/lackeyjb/playwright-skill
---

# Playwright Browser Automation

General-purpose browser automation skill. Write custom Playwright code for any automation task.

## Critical Workflow

1. **Auto-detect dev servers** - For localhost testing, ALWAYS run detection FIRST
2. **Write scripts to /tmp** - NEVER write test files to project directory
3. **Use visible browser by default** - `headless: false` unless user requests headless
4. **Parameterize URLs** - Make URLs configurable via constant at top of script

## Setup (First Time)

```bash
cd $SKILL_DIR && npm run setup
```

## Execution Pattern

**Step 1: Detect dev servers**
```bash
node -e "require('./lib/helpers').detectDevServers().then(s => console.log(JSON.stringify(s)))"
```

**Step 2: Write test script to /tmp**
```javascript
// /tmp/playwright-test-page.js
const { chromium } = require('playwright');

const TARGET_URL = 'http://localhost:3001'; // Auto-detected

(async () => {
  const browser = await chromium.launch({ headless: false });
  const page = await browser.newPage();
  await page.goto(TARGET_URL);
  console.log('Page loaded:', await page.title());
  await page.screenshot({ path: '/tmp/screenshot.png', fullPage: true });
  await browser.close();
})();
```

**Step 3: Execute**
```bash
node run.js /tmp/playwright-test-page.js
```

## Common Patterns

### Test Responsive Design
```javascript
const viewports = [
  { name: 'Desktop', width: 1920, height: 1080 },
  { name: 'Tablet', width: 768, height: 1024 },
  { name: 'Mobile', width: 375, height: 667 },
];

for (const viewport of viewports) {
  await page.setViewportSize({ width: viewport.width, height: viewport.height });
  await page.goto(TARGET_URL);
  await page.screenshot({ path: `/tmp/${viewport.name.toLowerCase()}.png`, fullPage: true });
}
```

### Test Login Flow
```javascript
await page.goto(`${TARGET_URL}/login`);
await page.fill('input[name="email"]', 'test@example.com');
await page.fill('input[name="password"]', 'password123');
await page.click('button[type="submit"]');
await page.waitForURL('**/dashboard');
console.log('✅ Login successful');
```

### Check for Broken Links
```javascript
const links = await page.locator('a[href^="http"]').all();
for (const link of links) {
  const href = await link.getAttribute('href');
  const response = await page.request.head(href);
  if (!response.ok()) {
    console.log(`❌ Broken: ${href} (${response.status()})`);
  }
}
```

## Tips

- **CRITICAL: Detect servers FIRST** - Always run `detectDevServers()` before testing
- **Use /tmp for test files** - Auto-cleanup, no project clutter
- **DEFAULT: Visible browser** - Use `headless: false` unless explicitly requested
- **Slow down:** Use `slowMo: 100` to make actions visible
- **Wait strategies:** Use `waitForURL`, `waitForSelector`, `waitForLoadState` instead of fixed timeouts
- **Error handling:** Always use try-catch

## Troubleshooting

- **Playwright not installed:** Run `npm run setup`
- **Browser doesn't open:** Check `headless: false`
- **Element not found:** Add wait: `await page.waitForSelector('.element', { timeout: 10000 })`
