## 👥 Team Workflow

- Each team member works on a separate branch:

```bash
git checkout -b feature/your-name
git push -u origin feature/your-name
```

- Make changes → commit → push:

```bash
git add .
git commit -m "add: feature description"
git push origin feature/your-name
```

### 🔁 Merging a branch into `main`

Once you finish your feature:

1. Push your branch (if not already pushed):

```bash
git push origin feature/your-name
```

2.Go to the GitHub repo: 
3.Click on **"Compare & pull request"**
4.Write a short description of what you added or changed
5.Click **"Create pull request"**
6.Another team member reviews and clicks **"Merge pull request"** into `main`

> Make sure you pulled the latest `main` before starting to avoid conflicts:

```bash
git checkout main
git pull origin main
```

> Then update your branch:

```bash
git merge feature/your-name
git push origin main
```

Resolve any conflicts before pushing.

---

🔒 Closing Issues Automatically

You can link your commits or Pull Requests to issues so they close automatically after merge:

> In your commit message, use keywords like closes, fixes, or resolves followed by the issue number:

```bash
git commit -m "fix: [short description] closes [#id]"
```

> If you want to close multiple issues in one commit/PR:

```bash
git commit -m "fix: [short description] closes [#id] closes [#id]"
```

> Alternatively, you can reference them in the Pull Request description:

```bash
This PR [short description]
Closes [#id]  
Closes [#id]
```

👉 Once the Pull Request is merged into main, GitHub will automatically close the mentioned issues.
<<<<<<< HEAD

---

📝 Conventional Commit Messages

To keep commit messages clean and consistent, use Conventional Commits:

> `feat:` → a new feature

```bash
git commit -m "feat: add user profile page"
```

> `fix:` → a bug fix

```bash
git commit -m "fix: login redirect issue"
```

> `docs:` → documentation changes only (e.g., README updates)

```bash
git commit -m "docs: update setup instructions"
```

> `style:` → code style/formatting (no logic change)

```bash
git commit -m "style: format code with Prettier"
```

> `refactor:` → code changes that neither fix a bug nor add a feature

```bash
git commit -m "refactor: simplify database query"
```

> `test:` → adding or fixing tests

```bash
git commit -m "test: add unit tests for login service"
```

> `chore:` → maintenance tasks, configs, build scripts

```bash
git commit -m "chore: update dependencies"
```

✅ Tip: Using these prefixes helps the team quickly understand the purpose of each commit and makes changelogs/releases easier to generate.
=======
>>>>>>> b74a826735508fe782186fbddcc14243c55d8b1b
