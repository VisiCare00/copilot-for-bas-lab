# Section 4 · Change management — commits & pull requests

⏱ **15 minutes** · 🎯 Save your change, open a "page review" (PR), and publish it.

## The translation guide

Forget the engineering words. Use these:

| GitHub term | What we'll call it today |
|---|---|
| Branch | **Draft copy** — a private workspace for your edits |
| Commit | **Save with a note** — a snapshot you can comment on later |
| Pull Request (PR) | **Page review** — your draft put forward for approval |
| Review comment | **Inline comment** — same as Confluence |
| Merge | **Publish** — your change is now the live version |

If anyone says "branch" or "merge", just nod and translate it in your head.

## Step 1 · Make a small edit on a draft copy (5 min)

1. In your editor (github.dev or VS Code Desktop), open the user story you created in section 3.
2. Add one sentence to the Context — anything. e.g. *"This story addresses the gap raised in last week's BA review."*
3. Save (`Ctrl+S`).
4. Click the **Source Control** icon in the left sidebar (it looks like a Y / branch glyph).
5. You'll see your file under "Changes". Type a short note in the message box: `Add review-context note`.
6. Click the **✓ Commit & Push** button.

> 🪪 If asked "do you want to create a new branch?", say **yes** and accept the suggested name. That's your "draft copy".

## Step 2 · Open the page review (5 min)

**If you're using github.dev:** after the commit, github.dev offers a button: **Create Pull Request**. Click it.

**If you're using VS Code Desktop:** there's no PR button in the editor by default. Open your fork on **github.com** in a browser — you'll see a yellow banner *"Your branch had recent pushes — Compare & pull request"*. Click it.
*(For a slicker desktop experience next time, install the **GitHub Pull Requests** extension — see [VSCODE-NOTES.md](../VSCODE-NOTES.md#3--creating-the-pull-request-after-a-commit-section-4-️-the-main-difference).)*

Whichever path you took, you're now on the PR page:

1. **Title:** something plain-English, e.g. `Add patient-history user story`.
2. **Description:** one or two sentences. *"Adds US-XXX. Context refined with Copilot."*
3. Click **Create**.
4. **Open the PR on github.com** (in a browser tab) so you can see the rendered view. Click **Files changed** at the top, then look for the **Source ↔ Rendered** toggle (top-right of the file) and pick **Rendered**. The page now looks like Confluence track-changes.

> 💡 The Rendered toggle only exists on github.com — not inside VS Code Desktop or the GitHub PR extension. Always hop to the browser for review-by-eye.

## Step 3 · Publish (3 min)

1. Back on the **Conversation** tab of your PR.
2. Click **Merge pull request** → **Confirm merge**.
3. Click **Delete branch** when offered. (It just tidies up your draft copies.)
4. Your change is now on the main page. Visit your fork's repo home — see the file updated.

## Why this is better than Confluence "track changes"

- The PR is a **conversation** — comments live on individual lines forever, not in a sidebar that disappears on save.
- The PR can require **approvals** before publishing — a real governance gate, not a polite "please review" email.
- Every published change has a **reason and a reviewer** attached, not just a timestamp.

## Checkpoint ✅

- [ ] You opened, reviewed and merged a Pull Request in your fork.
- [ ] Your change is now visible on the main page of the file.
- [ ] React 👍 in the lab chat.

> ➡️ Next: [05 · End-to-end](../05-end-to-end/) — close the loop.
