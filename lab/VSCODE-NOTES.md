# VS Code Desktop notes — for attendees not using github.dev

> The lab instructions are written assuming **github.dev** (the browser editor). If you're using **VS Code Desktop** on your laptop, 95% of the steps are identical. This page covers the **four moments where they differ**.

If you're using github.dev, you can ignore this whole page.

---

## 1 · Getting your fork onto your laptop (Section 0)

**github.dev:** press `.` on the fork's github.com page. Done.

**VS Code Desktop:**

1. On your fork's github.com page, click the green **Code** button.
2. Choose **Open with GitHub Desktop**, OR
   - Copy the HTTPS URL, then in VS Code: `Ctrl+Shift+P` → **Git: Clone** → paste the URL → choose a folder.
3. Open the cloned folder in VS Code (it usually offers).
4. **Accept the "Install recommended extensions" prompt** when it appears — Foam, Markdown Preview Enhanced and others light up the wiki experience.

> ⏱️ Adds about 1 minute to Section 0. Catch up by skipping ahead while the clone runs.

---

## 2 · Sign-in popup (first time only)

The first time you use Source Control or Copilot in VS Code Desktop, you'll get a popup asking to **sign in to GitHub**.

1. Click **Allow** / **Sign in with browser**.
2. A browser tab opens. Approve the access.
3. Return to VS Code — the popup closes itself.

This doesn't happen in github.dev because you're already signed in via the browser.

---

## 3 · Creating the Pull Request after a commit (Section 4) ⚠️ The main difference

**github.dev:** after **Commit & Push**, a button appears offering to **Create Pull Request** in the same window.

**VS Code Desktop:** no PR button appears by default. You have two options:

### Option A — Open the PR on github.com (simplest)

1. After **Commit & Push**, open your fork on github.com in a browser.
2. GitHub shows a yellow banner at the top: *"Your branch had recent pushes — Compare & pull request"*.
3. Click **Compare & pull request**, fill in title + description, click **Create pull request**.

### Option B — Install the GitHub Pull Requests extension (one-time, nicer)

1. In VS Code: Extensions panel (`Ctrl+Shift+X`) → search for **GitHub Pull Requests** → install.
2. Sign in when prompted.
3. After your next commit, the SCM sidebar shows a **Create Pull Request** view. Fill it in there.
4. Review and merge directly from VS Code.

> If you're trying this for the first time tomorrow, **use Option A** — it's the fastest path during the lab. Install the extension afterwards if you want the slicker desktop experience.

---

## 4 · Viewing the PR as a "Rendered" page (Section 4)

The **Rich diff / Rendered** toggle that makes a Markdown PR look like a Confluence track-changes view is a **github.com** feature — it does not exist inside VS Code Desktop or the GitHub PR extension.

To see it:

1. On your PR, click **Files changed** at the top.
2. Look for the toggle **Source** ↔ **Rendered** (top-right of the file). Pick **Rendered**.

You can review code and comments inside VS Code, but for the rendered Markdown experience, hop to the browser.

---

## What else?

Everything else is genuinely identical:

| Activity | github.dev | VS Code Desktop |
|---|---|---|
| Editing files, save, preview | ✅ same | ✅ same |
| Copilot Chat, slash-prompts | ✅ same | ✅ same |
| Source Control panel, commits | ✅ same | ✅ same |
| `Ctrl+Shift+F` search | ✅ same | ✅ same |
| Foam wiki-links (`[[Page]]`), backlinks | partial | ✅ full |
| Foam graph view | partial | ✅ full |
| Issues, Project board | both done on github.com in a browser | both done on github.com in a browser |

---

## If you get stuck

Drop a message in the lab chat. The four differences above cover ~95% of what trips desktop users up. Anything weirder goes in [STUCK.md](../STUCK.md).
