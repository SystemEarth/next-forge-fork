# Next-forge

Link: [https://docs.next-forge.com/setup](https://docs.next-forge.com/setup)

## Create Next-forge source

```bash
brew install pnpm
npx next-forge@latest init .
pnpm setup 
pnpm add -g @mintlify/cli #Install mintlify
source ~/.zshrc
# setup stripe
# setup env var: clerk, stripe, betterstack, resend, etc ...
pnpm dev
```

## Bump Next-forge version

Commit version changes and fixes without commit/author bloat.

```bash
git remote add upstream <git-ssh-link>
git fetch upstream
git cherry-pick <commit-hash>
git cherry-pick <start-commit>^..<end-commit>
resolve conflicts
git cherry-pick --continue
git merge upstream/main --squash
```

Remove extra files.

```bash
rm -rf Splash
rm -rf Docs (this is distinct and not Apps/Docs)
rm -rf Scripts
rm .github/CONTRIBUTING.md .github/FUNDING.yml .github/SECURITY.md
rm -rf .github/workflows
rm license.md CHANGELOG.md .autorc
```
