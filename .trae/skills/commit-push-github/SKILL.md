---
name: commit-push-github
description: Commit and push the current project to the GitHub repository. Use when the user asks to commit and push the project or sync code to the GitHub remote. Do not use for other git operations.
---

# Commit and Push to GitHub

## Workflow

1. Check status: `git status`
2. Stage all changes: `git add -A`
3. Check staged changes: `git diff --cached --stat`
4. Commit with a descriptive message summarizing the changes
5. Push to the GitHub remote: `git push github master`
   - First push needs upstream tracking: `git push -u github master`

## Important Notes

- Git is not in PATH on this machine; use the full path:
  `D:\大一第一个学期\导引\Git\cmd\git.exe`
- The GitHub repository is `https://github.com/LZY527-hub/lizhiyun`
- SSH public key is already configured, so use the SSH URL:
  `git@github.com:LZY527-hub/lizhiyun.git`
- The `origin` remote is already used by Gitee (`https://gitee.com/li-zhiy/lizhiyun527.git`);
  add GitHub as a separate remote named `github`:
  `git remote add github git@github.com:LZY527-hub/lizhiyun.git`
- If the `github` remote already exists with a different URL, update it:
  `git remote set-url github git@github.com:LZY527-hub/lizhiyun.git`
- The local branch is `master`; if the GitHub repo's default branch is `main`, either push with
  `git push -u github master:main` or keep pushing `master` as-is per the user's choice
- Always write clear, concise commit messages in Chinese or English matching the repo style
- If push fails because the remote has diverged, use `git pull --rebase github master` before retrying
- If SSH auth fails, verify with `ssh -T git@github.com` and ask the user to check their key

## Example Commit Messages

- `feat: 添加新页面`
- `fix: 修复样式问题`
- `chore: 更新项目文件`
