# Drawing Board — Chrome Web Store Submission Package

Copy-paste these straight into the Developer Dashboard. Everything here is
matched line-by-line to what's actually in manifest.json and the code — no
permission or claim listed here that isn't real.

---

## 1. Store Listing Tab

**Extension name** (max 75 chars — this one is 42)
```
Drawing Board – Instant Whiteboard Overlay
```

**Summary** (max 132 chars — shown under the name in search results; this one is 128)
```
Draw flowcharts, shapes, connectors, and sticky notes directly on top of any webpage — no new tab, no sign-up, instant overlay.
```

**Category**
```
Productivity
```

**Language**
```
English (you can add Bahasa Malaysia as a second listing language later if you want local reach)
```

**Detailed description** (long-form, paste into the "Description" field)
```
Drawing Board turns any webpage into an instant whiteboard. Press Alt+D (or
Cmd+Shift+D on Mac) or click the toolbar icon, and a full-page diagramming
canvas appears on top of the site you're looking at — no new tab, no
account, nothing to configure.

WHY DRAWING BOARD
Most diagramming tools make you leave the page you're working from and
rebuild context in a separate app. Drawing Board skips that: you sketch
directly on top of the article, dashboard, design mock-up, or document
you're already looking at, then export or close it when you're done.

WHAT YOU CAN DRAW
• Shapes — rectangle, rounded rectangle, ellipse, and diamond (decision) nodes
• Connectors — straight arrows, plain lines, and curved lines, with
  automatic snap-to-anchor so connectors stay attached to shapes as you
  move them
• Freehand pen and highlighter for quick annotations
• Text notes — double-click to type, click away to save
• A Nord-inspired minimalist color palette

TWO BOARD MODES
• Transparent Overlay — draw directly on top of the live page underneath
• Grid / Dot Board — a clean whiteboard backdrop for pure diagramming,
  independent of the page behind it

BUILT FOR SPEED
• Select, drag, and resize any shape with corner handles
• Undo / redo (Ctrl+Z / Ctrl+Shift+Z)
• Drag the toolbar anywhere on screen — it remembers where you left it
• Minimize to a small tab and bring the board back with one click
• Your drawing is saved automatically per page, so it's still there if you
  close and reopen the overlay on the same URL

EXPORT YOUR WORK
• Export as PNG for sharing in chats, docs, or tickets
• Export as SVG for further editing in design tools
• Export as JSON if you want the raw shape data

PRIVACY BY DESIGN
Drawing Board has no backend server and no analytics. Everything you draw
is stored locally on your device using Chrome's built-in storage — it is
never uploaded anywhere. Full privacy policy linked in the listing.

WHO IT'S FOR
Consultants explaining a flow on a client's live site, developers sketching
architecture over documentation, teachers annotating a webpage during a
lesson, or anyone who needs to think visually without leaving the tab
they're already on.
```

---

## 2. Privacy Practices Tab

**Single purpose description** (required field — one or two sentences)
```
Drawing Board lets users draw diagrams, shapes, connectors, and annotations
in a full-page overlay on top of the currently active webpage, triggered
only by explicit user action (icon click or keyboard shortcut).
```

**Permission justifications** (paste one per permission field)

| Permission | Justification (paste as-is) |
|---|---|
| `activeTab` | "Used to inject the drawing overlay only into the tab the user is currently viewing, and only when the user explicitly clicks the extension icon or presses the keyboard shortcut. The extension never accesses tabs the user has not directly activated it on." |
| `scripting` | "Used to inject the overlay's canvas, toolbar, and stylesheet into the active tab at the moment the user triggers the extension. No script is injected automatically or on page load." |
| `storage` | "Used with chrome.storage.local to save the user's drawings (per page URL) and the toolbar's on-screen position, entirely on-device. No data is transmitted off the device." |

**Are you using remote code?**
```
No — all code ships inside the extension package.
```

**Data usage — "What user data do you plan to collect?"**
Answer **None** / leave every category unchecked (Personally identifiable
info, Health info, Financial info, Authentication info, Personal
communications, Location, Web history, User activity, Website content).
The extension does not transmit any data anywhere — everything is written
only to `chrome.storage.local` on the user's own machine.

**Certify data usage compliance**
```
✓ I do not sell or transfer user data to third parties, outside of the approved use cases
✓ I do not use or transfer user data for purposes unrelated to the item's single purpose
✓ I do not use or transfer user data to determine creditworthiness or for lending purposes
```
(All three are true for this extension — check them.)

**Privacy policy URL**
```
[Faiz — host privacy-policy.html at a public URL first, e.g.:
https://drfaizazizan.com/drawing-board/privacy-policy.html
or GitHub Pages: https://<username>.github.io/drawing-board/privacy-policy.html
Chrome Web Store requires a live URL here, not pasted text.]
```

---

## 3. Assets Checklist

| Asset | Requirement | Status |
|---|---|---|
| Icon 16×16 | required | ✅ included (`icons/icon16.png`) |
| Icon 48×48 | required | ✅ included (`icons/icon48.png`) |
| Icon 128×128 | required | ✅ included (`icons/icon128.png`) |
| Screenshots | 1–5 images, 1280×800 or 640×400 | ❌ not generated here — needs a real browser. Take 2–3: (1) overlay drawing over a normal site, (2) toolbar close-up with shapes/connectors, (3) grid board mode |
| Small promo tile | 440×280, optional but recommended | ❌ not generated — nice-to-have, not blocking |
| Marquee promo tile | 1400×560, optional | ❌ skip unless you want featured placement |

---

## 4. Confirmed vs Not Verifiable

**✅ Confirmed (static checks run in this sandbox):**
- `manifest.json` is valid JSON, `manifest_version: 3`, `background.service_worker` present
- No `eval()`, no inline event handlers, no remote script loading, no inline `<script>`
- Every declared permission (`activeTab`, `scripting`, `storage`) is actually used in the code — no unused permissions to flag
- Extension name: 42/75 chars · Summary: 128/132 chars · manifest `description`: 100/132 chars
- Icons present at all three required sizes

**❓ Not verifiable here (needs Faiz to confirm by testing / uploading):**
- Actual runtime behavior in real Chrome (permission prompts, real rendering on live sites, drag/resize feel)
- Screenshots and promo tiles — need a real browser session to capture
- Whether "Drawing Board" or close variants are already taken as a listing name on the Web Store (worth a quick search before submitting)
- Actual review outcome — Google's review process is the only source of truth on approval

**Faiz still needs to do himself:**
- Host `privacy-policy.html` at a public URL and paste that URL into the Privacy Practices tab
- Take screenshots and upload them
- Pay the $5 one-time developer registration fee (if not already registered) and click Submit — that step requires his own Developer Dashboard account and cannot be done on his behalf
