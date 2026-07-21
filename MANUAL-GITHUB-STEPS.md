# Manual GitHub Setup Steps

I don't have a connected GitHub account, so I can't delete `Workflows`, create `AI-Projects`, or push commits for you. Here's exactly what to run once you download the `AI-Projects.zip` package.

## 1. Create the new repository

On GitHub:
1. Go to **github.com/new**.
2. Repository name: `AI-Projects`.
3. Visibility: your choice (Public recommended if this is for recruiters/clients).
4. **Do not** initialize with a README/gitignore/license — you already have those.
5. Click **Create repository**.

## 2. Push the local files

```bash
# Unzip the package I gave you, then:
cd AI-Projects
git init
git add .
git commit -m "Initial commit: restructured AI agent portfolio"
git branch -M main
git remote add origin https://github.com/Maruthi-builds/AI-Projects.git
git push -u origin main
```

## 3. Delete (or archive) the old Workflows repository

GitHub doesn't allow deletion via script/API without a token with `delete_repo` scope, so do this manually:
1. Go to `https://github.com/Maruthi-builds/Workflows/settings`.
2. Scroll to the **Danger Zone**.
3. Click **Delete this repository** (or **Archive this repository** if you'd rather keep it read-only/backed up instead of deleting).
4. Confirm by typing the repository name when prompted.

> 💡 If `Workflows` has commit history or content you haven't fully migrated, consider archiving instead of deleting — it becomes read-only but stays recoverable.

## 4. Before making it public — personalize the workflows

Two things to check before you publish:

1. **`ai-executive-assistant-agent`** — the agent system prompts contain a real third-party name and company email address that isn't yours. Open `workflow/executive-assistant-workflow.json`, find the `Email Assistant`, `Follow Up Assistant`, `Master Orchestrator Agent`, and `Slack Assistant` nodes, and replace the name/email/Slack ID with your own (or genericize them) before pushing publicly.
2. **All credential references** (e.g. `"name": "OpenAi account 4"`) are just internal n8n labels, not secrets — but double-check none of your real API keys, tokens, or spreadsheet/document IDs that you consider sensitive are in the JSON before making the repo public. Spreadsheet/Doc IDs in this export (contacts sheet, Pinecone index name, etc.) are visible — swap them for placeholders if you'd rather not expose them.

## 5. Repo settings polish (optional but recommended)

- Add a short repo description + topics (`n8n`, `ai-agents`, `automation`, `llm`) in the GitHub repo settings sidebar — this is what shows up in search and on your profile.
- Pin `AI-Projects` to your GitHub profile (Profile → Customize your pins).
- Add a social preview image if you want it to look sharp when shared as a link.
