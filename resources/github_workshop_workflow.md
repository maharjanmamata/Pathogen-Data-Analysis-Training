# GitHub Desktop Workflow Guide

This guide is designed to help you use **GitHub Desktop** for research collaborations. It includes basic setup, best practices, and how to work collaboratively with others.

---

## 🚀 Getting Started with GitHub Desktop

### 1. Clone the Workshop Repository
- Open GitHub Desktop.
- Go to `File > Clone Repository`.
- Select the workshop repository (provided by the instructor).
- Choose a local folder (e.g., inside your `Documents` or a `workshop` folder).

### 2. Make Your Own Branch
- In GitHub Desktop, switch to the "Current Branch" dropdown.
- Click `New Branch` and name it something like `my-edits` or `analysis-day1`.
- This keeps your changes organized and separate from others.

### 3. Make Edits Locally
- Open files using RStudio or your preferred editor.
- Make changes (e.g., run code, save notebooks, add notes).

### 4. Commit Changes
- In GitHub Desktop, you’ll see file changes listed.
- Add a clear summary (e.g., `cleaned metadata`, `ran TAC heatmap code`).
- Click `Commit to branch-name`.

### 5. Push to GitHub
- After committing, click `Push origin` to upload your changes to GitHub.
- You may need to log into GitHub if prompted.

### 6. Pull Request
- If you want to commit your changes to the main repository from your branch, submit a pull request
- The administrator/owner of the main repo will review and accept your request
- Changes made in your branch will be merged with the main repo
---


## 🔁 Forking vs. Branching: Which to Use?

### Forking (for long-term/public contributions)
- **Creates your own copy** of the instructor’s repo under your GitHub account.
- Best if you want to keep working after the workshop or submit pull requests.
- **Steps:** Fork → Clone → Work → Push → Pull Request.

### Branching (for in-workshop collaboration)
- **Creates a new branch** within the shared workshop repo.
- Best for short-term edits when you have write access.
- Easier to help troubleshoot during the workshop.


### Instructor Recommendation
| Goal                        | Recommendation                          |
|-----------------------------|-------------------------------------------|
| Fast setup, minimal errors  | Clone repo → work on branches or locally |
| Teach collaboration basics  | Use branches within a shared repo        |
| Teach open-source workflows | Fork → Pull request                      |

---

## 📦 Best Practices

### ✅ Do
- Pull before you start work to get the latest version.
- Commit often with clear messages.
- Use branches to isolate changes.
- Ask for help if you run into a Git conflict.

### 🚫 Avoid
- Editing files on the `main` branch.
- Working without pulling latest changes.
- Copying files manually instead of tracking changes.

---

## 🧠 Bonus Tips

### Syncing New Files from Instructor
If your instructor adds new files during the workshop:
- Pull changes from `main` (or upstream repo if you forked).
- Merge into your working branch if needed.

### Resetting a Broken Repo (if needed)
If things go wrong:
- Delete the local folder.
- Clone the repository again from GitHub Desktop.

---

## 🔗 Resources
- [GitHub Desktop Documentation](https://docs.github.com/en/desktop)
- [Happy Git and GitHub for the useR](https://happygitwithr.com/) (great for R users)
- [GitHub Training Videos](https://lab.github.com/)

---

Let an instructor or TA know if you get stuck!

