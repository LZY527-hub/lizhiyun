---
name: commit-push-gitee
description: Use when the user asks to commit and push the current project to the Gitee repository. Runs git add, git commit, and git push to https://gitee.com/li-zhiy/lizhiyun527.git.
---

# Commit and Push to Gitee

## Workflow

1. Check status: `git status`
2. Stage all changes: `git add -A`
3. Check staged changes: `git diff --cached --stat`
4. Commit with a descriptive message summarizing the changes
5. Push to the Gitee remote: `git push origin main`
   - If the branch is not `main`, use the actual branch name: `git push origin HEAD`

## Important Notes

- The remote repository URL is `https://gitee.com/li-zhiy/lizhiyun527.git`
- If no remote is configured, add it first:
  `git remote add origin https://gitee.com/li-zhiy/lizhiyun527.git`
- If the remote already exists with a different URL, update it:
  `git remote set-url origin https://gitee.com/li-zhiy/lizhiyun527.git`
- Always write clear, concise commit messages in Chinese or English matching the repo style
- If push fails due to auth, ask the user to check their Gitee credentials
- If push fails because remote has diverged, use `git pull --rebase origin main` before retrying

## Example Commit Messages

- `feat: 添加新页面`
- `fix: 修复样式问题`
- `chore: 更新项目文件`
