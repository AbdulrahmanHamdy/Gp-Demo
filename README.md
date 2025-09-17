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
