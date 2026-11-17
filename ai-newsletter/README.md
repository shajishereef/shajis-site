# Issue page template

Every issue page shares one stylesheet, `issue.css`, which matches the homepage design.
When the weekly task creates a new issue (`YYYY-MM-DD.html`, copied to `index.html`):

1. **Don't write a `<style>` block.** In `<head>`, include the Newsreader / Geist / Geist Mono font link, the early theme script and `<link rel="stylesheet" href="issue.css">`. Copy these from the latest issue.
2. **Copy the page frame from the latest issue:**
   - the `<header class="bar">` top bar, with links back to `../`
   - `<main class="wrap">`
   - the `.header` block: the `.meta` row (issue number, week range, date), the `.kicker`, an `<h1>` with the issue title only, and a `.sub` row of topic `<span>`s
   - `.intro`, the filter `.panel`, `#board`, `.summary-grid`, `.fd-bottom-bar` and `footer.footer`
3. **Keep the class names the script uses:** `upd-card`, `upd-head`, `upd-num`, `upd-title`, `upd-tag`, `maker`, `card-foot`, `mini`, `readbtn`, `reality`, `sum-card`, `sc-title`, `hl-*`.
4. **Increase the issue number** in `.meta`. It should equal that issue's position in `issues.js`, counting from the oldest.
5. **Add the issue to `issues.js`** as before. The homepage reads the archive from it.
