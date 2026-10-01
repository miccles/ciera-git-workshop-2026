# Git & GitHub for Research — practice repository
CIERA · Monday October 26, 2026 · 1:00–2:30 p.m.

This is a fictional, text-only analysis configuration. No science software, real data or cluster access is required. Values are teaching examples, not scientific recommendations.

## Get ready
Open this repository folder itself in VS Code, then Source Control and the integrated terminal. Git must be installed separately. A GitHub account is not needed for the local exercise.

This starter has three commits on main and an example branch, sensitivity-example, for looking at history. Stay on main for the optional exercise. Do not create a repository inside an existing research project.

Set your name and email for your copy (these commands do not change global settings):
```bash
git config user.name "Your Name"
git config user.email "you@example.edu"
git status
git log --oneline --graph --decorate --all
```
Choose an email you are comfortable publishing if you later share commits.

## Optional exercise — about six minutes
1. Open analysis-config.txt. Change threshold = 0.05 to another value, such as 0.03. Add a comment beginning with # explaining why.
2. Save. In Source Control, open the file under Changes and inspect the diff.
3. Stage only analysis-config.txt with its + button, then inspect it under Staged Changes.
4. Before committing, explain to a neighbor what you are about to record.
5. Enter a meaningful message and commit. Check history and status.

Terminal equivalents (edit the file using your editor):
```bash
git status
git diff
git add analysis-config.txt
git diff --staged
git commit -m "Adjust threshold for the practice analysis"
git log --oneline -3
git status
```
Done: your commit contains the intended setting and reason, with no other pending changes. You have not published anything to GitHub.

Stretch: after staging, edit the file again. Compare git diff and git diff --staged. The new edit stays unstaged; a clean status is not expected during the stretch. Keep the new edit by staging/committing it if you want it.

## Branches, if you want to explore after the demonstration
```bash
git switch -c my-experiment
# Edit and save analysis-config.txt; then stage and commit your change.
git switch main
git merge my-experiment
```
Start with a clean status. With main unchanged, this normally fast-forwards; it need not create a merge commit. The instructor will demonstrate diverged branches and a conflict separately. The existing sensitivity-example branch is for inspection; do not merge it during the six-minute exercise.

## Files and limits
- analysis-config.txt: fictional target, threshold and output directory.
- .gitignore: generated results, caches, environment files and local secrets.
- README.md: instructions you are reading.

There is no executable analysis or test suite. Review the final configuration text and history; do not claim a scientific result has been validated. If the folder lacks .git because you downloaded a ZIP, ask for clone/bundle instructions: a ZIP does not preserve commit history.
