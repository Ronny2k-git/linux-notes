# Work
 
Commands I reach for daily on development machines.
 
## Git (general)
 
| Command | What it does |
|---|---|
| `git config --global user.name “username” ` | Connection to github |
| `git config --global user.email “email”` |Connection to github |
| `git status` | check repository status |
| `git add .` | stage all changes |
| `git commit -m "message"` | create a commit |
| `git push` | upload commits to remote |
| `git pull` | download and merge remote changes |
| `git log --oneline` | view commit history |
| `git diff` | show unstaged changes |
| `git diff --staged` | show what's about to be committed |
| `git checkout -b` | Create a new branch and redirect |
| `git checkout branch name` | Go to selected branch |
| `git branch -a` | list local and remote branches |
| `git switch branch` | switch branch |
| `git switch -c new-branch` | create branch and switch to it |
| `git clone url` | clone a repository |
 
### Git - Undoing things 
 
| Command | What it does |
|---|---|
| `git restore file` | discard unstaged changes to a file |
| `git restore --staged file` | unstage a file, keep the changes |
| `git commit --amend` | fix the last commit message or add to it |
| `git reset --soft HEAD~1` | undo last commit, keep the changes staged |
| `git reset --hard HEAD` | throw away all local changes — **no undo** |
| `git stash` | save changes temporarily |
| `git stash apply` | bring them back |
| `git stash list` | Stash list|
| `git stash clear` | Clear stash list |
| `git revert commit-hash` | undo a pushed commit safely |
 
> `reset` rewrites history — fine locally, dangerous if already pushed. `revert` makes a new commit that undoes the old one, which is the safe option on a shared branch.
 
## GitHub CLI
 
| Command | What it does |
|---|---|
| `gh auth login` | authenticate |
| `gh repo clone owner/repo` | clone |
| `gh repo create name --public --source=. --push` | create repo from current folder |
| `gh pr create` | open a pull request |
| `gh pr list` | list open PRs |
| `gh repo view --web` | open current repo in browser |
 
## SSH
 
| Command | What it does |
|---|---|
| `ssh user@host` | connect to a remote machine |
| `ssh-keygen -t ed25519 -C "email"` | generate an SSH key |
| `ssh-copy-id user@host` | install your key on the server — stop typing passwords |
| `scp file user@host:/path/` | copy a file to a remote machine |
| `scp -r folder user@host:/path/` | copy a folder |
| `scp user@host:/path/file .` | copy **from** remote to here |
 
## Processes & ports
 
| Command | What it does |
|---|---|
| `lsof -i :3000` | find what's using port 3000 |
| `kill -9 $(lsof -t -i:3000)` | kill whatever is on port 3000 |
| `ss -tulpn` | show listening ports and processes |
| `pgrep -a node` | find running node processes |
 
## Project
 
| Command | What it does |
|---|---|
| `tree -L 2` | project structure, two levels deep |
| `tree -I node_modules` | ignore a folder |
| `file filename` | identify a file type |
| `du -sh * \| sort -h` | what's taking up space |
| `wc -l file` | count lines |
| `grep -rn "TODO" --exclude-dir=node_modules .` | find TODOs, skip deps |
 
## Node & package managers
 
| Command | What it does |
|---|---|
| `npm install` / `bun install` | install dependencies |
| `npm run dev` / `bun dev` | run a script |
| `npx package` / `bunx package` | run without installing |
| `npm outdated` | what's out of date |
| `node -v` · `npm -v` · `bun -v` | versions |
 
---