# claude-training

Repository for Claude Code training exercises and experiments.

The project is mirrored on two remotes:

| Remote | URL |
| ------ | --- |
| GitHub | `git@github.com:vietduongquoc-agilityio/claude-training.git` |
| GitLab | `git@gitlab.asoft-python.com:viet.duong/claude-training.git` |

---

## Prerequisites

- [Git](https://git-scm.com/) 2.30+
- An SSH key added to your GitHub and/or GitLab account
  ([GitHub guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh),
  [GitLab guide](https://docs.gitlab.com/ee/user/ssh.html))
- [Claude Code](https://docs.claude.com/en/docs/claude-code/overview) (optional, for the exercises)

Check your SSH access:

```bash
ssh -T git@github.com
ssh -T git@gitlab.asoft-python.com
```

---

## Getting started

### 1. Clone the repository

From GitHub:

```bash
git clone git@github.com:vietduongquoc-agilityio/claude-training.git
cd claude-training
```

Or from GitLab:

```bash
git clone git@gitlab.asoft-python.com:viet.duong/claude-training.git
cd claude-training
```

### 2. Set your Git identity for this repo

```bash
git config user.name "Your Name"
git config user.email "you@example.com"
```

### 3. Check out the working branch

```bash
git fetch origin
git switch feature/claude-training
```

---

## Push to GitHub and GitLab at once (optional)

To make a single `git push` update both remotes, add both URLs as push targets of `origin`:

```bash
git remote set-url --add --push origin git@github.com:vietduongquoc-agilityio/claude-training.git
git remote set-url --add --push origin git@gitlab.asoft-python.com:viet.duong/claude-training.git
```

Verify:

```bash
git remote -v
# origin  git@github.com:vietduongquoc-agilityio/claude-training.git (fetch)
# origin  git@github.com:vietduongquoc-agilityio/claude-training.git (push)
# origin  git@gitlab.asoft-python.com:viet.duong/claude-training.git (push)
```

Now `git push` sends your commits to both GitHub and GitLab.

---

## Branching workflow

| Branch | Purpose |
| ------ | ------- |
| `main` | Stable branch. No direct commits. Changes land through a pull/merge request. |
| `feature/claude-training` | Main working branch for training exercises. |
| `feature/<topic>` | Short-lived branches for individual exercises or features. |

Typical flow:

```bash
git switch main
git pull
git switch -c feature/<topic>
# ...make changes...
git add <files>
git commit -m "feat: short description"
git push -u origin feature/<topic>
```

Then open a Pull Request (GitHub) or Merge Request (GitLab) into `main`.

### Commit message convention

This repo follows [Conventional Commits](https://www.conventionalcommits.org/):

| Type | Use for |
| ---- | ------- |
| `feat` | New feature or exercise |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `chore` | Tooling, config, maintenance |

---

## Project structure

```text
claude-training/
├── .gitignore
└── README.md
```

The structure will grow as training exercises are added.
