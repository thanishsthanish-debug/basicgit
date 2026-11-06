# Travel Page: team challenge

A tiny HTML and CSS page. Your team of four (or five) builds it together using Git and GitHub.

## Roles

| Role | Who | Job |
|---|---|---|
| Dev 1 | one person | feature: navigation bar |
| Dev 2 | one person | feature: gallery |
| Dev 3 | only in teams of five | feature: footer |
| Reviewer / Tech Lead | one person | reviews every Pull Request, merges, tags the release |
| QA | one person | tests `main`, reports bugs as GitHub Issues |

## Setup (Reviewer first)

1. Click **Use this template > Create a new repository**. Make it **public**.
2. Settings > Collaborators: add your teammates.
3. Everyone accepts the invitation, then clones the repo and opens it in VS Code.

## Features

Work on your own branch. Make at least two small commits, using Conventional Commit messages (`feat:`, `fix:`, `style:`).

**Dev 1: `feature/navbar`**
Add a `<nav>` with three links (Home, Places, Contact) where it says `NAVBAR GOES HERE`. Style it at the end of `style.css`.

**Dev 2: `feature/gallery`**
Add a gallery section with three destination cards (name plus one line each) where it says `GALLERY GOES HERE`. Style it at the end of `style.css`.

**Dev 3 (teams of five only): `feature/footer`**
Add a `<footer>` with a contact email and a short line of text where it says `FOOTER GOES HERE`. Style it at the end of `style.css`.

Then: push your branch, open a Pull Request into `main`, and ask the Reviewer to review it.

Several of you edit the same lines. Git will report conflicts. That is expected: the developer whose Pull Request is merged later updates their own branch (`git pull origin main`), fixes the conflict markers, commits and pushes again.

## QA checklist

Open `index.html` in a browser on the latest `main` and check:

- [ ] The browser tab title reads **Travel Page**
- [ ] The heading and intro text are visible
- [ ] The navigation bar shows three links
- [ ] The gallery shows three cards
- [ ] The footer shows contact details (teams of five only)
- [ ] No leftover `<<<<<<<`, `=======` or `>>>>>>>` lines in any file

Report each problem as a GitHub Issue.

## Hotfix and release

For each bug: a developer branches from the latest `main` as `hotfix/<name>`, fixes it, opens a Pull Request, the Reviewer merges it. The Reviewer then tags the release:

```
git tag -a v1.0.1 -m "Hotfix release"
git push origin v1.0.1
```
