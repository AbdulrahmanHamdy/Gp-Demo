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

In your commit message, use keywords like closes, fixes, or resolves followed by the issue number:

git commit -m "fix: login redirect bug closes #3"


If you want to close multiple issues in one commit/PR:

git commit -m "feat: add image upload closes #3 closes #5"


Alternatively, you can reference them in the Pull Request description:

This PR adds login redirect handling and image upload.
Closes #3  
Closes #5


👉 Once the Pull Request is merged into main, GitHub will automatically close the mentioned issues.