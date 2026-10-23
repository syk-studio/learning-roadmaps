
# Git and GitHub — Complete Beginner's Guide

Welcome to Git and GitHub! Git helps you track changes in your code, while GitHub lets you store repositories online, collaborate with others, and contribute to open-source projects.

**Goal:** Learn version control, manage your projects with Git, and make your first open-source contribution.

**Prerequisites:** Basic command-line familiarity and some experience writing HTML, CSS, and JavaScript.

---

## How to Use This Guide

For each step:

1. Watch the recommended lecture or search for a suitable lesson.
2. Run the commands yourself in a practice repository.
3. Complete the exercises.
4. Make sure you understand what each command does before moving on.

**Video-link note:** The links below open YouTube searches, not individually verified videos. Choose a clear, current lecture covering the listed topics. Prefer one comprehensive tutorial per step when it covers everything required.

---

## Step 1: Understand Git and Version Control

### Learn

- What version control means
- Why developers use Git
- Git vs. GitHub
- Local and remote repositories
- Working directory, staging area, and commit history
- Basic Git terminology

### Watch

- [Git and GitHub for Beginners — Full Course](https://www.youtube.com/results?search_query=git+and+github+for+beginners+full+course)

### Practice

1. Explain Git in your own words.
2. Explain how Git differs from GitHub.
3. Identify the working directory, staging area, and repository in a simple Git workflow.

**Checkpoint:** You understand why version control matters and how Git and GitHub work together.

---

## Step 2: Install Git and Configure Your Environment

### Learn

- Installing Git on Windows, macOS, or Linux
- Opening a terminal or command prompt
- Checking the installed version
- Configuring your Git username and email
- Choosing a code editor with Git support

### Watch

- [Install and Configure Git for Beginners](https://www.youtube.com/results?search_query=install+git+windows+configure+username+email+beginner)

### Commands

Check your installation:

```bash
git --version
```

Configure your commit identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Check your configuration:

```bash
git config --global --list
```

Replace the example name and email with your own details. Use an email appropriate for your GitHub account; consider GitHub's private `noreply` email if you don't want to expose your personal email in commits.

### Practice

1. Install Git.
2. Run `git --version`.
3. Configure your name and email.
4. Verify your configuration.

**Checkpoint:** Git is installed and ready to use.

---

## Step 3: Create a Repository and Track Changes

### Learn

- Initializing a repository with `git init`
- Checking status with `git status`
- Understanding the working directory and staging area
- Staging files with `git add`
- Creating commits with `git commit`
- Writing useful commit messages

### Watch

- [Git Init, Add, Commit, and Status Explained](https://www.youtube.com/results?search_query=git+init+add+commit+status+beginner+tutorial)

### Practice

Create a folder for a small practice project and open a terminal inside it.

```bash
git init
git status
```

Create a `README.md` file, then run:

```bash
git add README.md
git status
git commit -m "docs: add project README"
git log --oneline
```

### Understand the workflow

1. Edit a file.
2. Check which files changed.
3. Stage the intended changes.
4. Commit the staged changes.
5. Review the commit history.

**Checkpoint:** You can create a local repository and save a snapshot of your work.

---

## Step 4: Inspect Changes and Undo Mistakes Safely

### Learn

- `git diff`
- `git diff --staged`
- `git log`
- `git show`
- `git restore`
- `git restore --staged`
- `git revert`
- The difference between restoring a file and reverting a commit

### Watch

- [Git Diff, Log, Restore, and Revert Explained](https://www.youtube.com/results?search_query=git+diff+log+restore+revert+beginner)

### Practice

1. Modify a file and inspect the changes using `git diff`.
2. Stage the file and inspect the staged changes.
3. Unstage it with `git restore --staged`.
4. Use `git log --oneline` to inspect commits.
5. Practice undoing changes in a disposable test repository.

**Important:** `git restore` can discard uncommitted work. Avoid destructive commands such as `git reset --hard` until you understand their effects. Never rewrite shared history without coordinating with collaborators.

**Checkpoint:** You can inspect your changes and choose an appropriate way to correct a mistake.

---

## Step 5: Work with .gitignore

### Learn

- What `.gitignore` does
- Ignoring generated files and local configuration
- Common entries such as `node_modules/`, build output, and `.env`
- Why `.gitignore` does not automatically untrack files already committed

### Watch

- [Git .gitignore Explained for Beginners](https://www.youtube.com/results?search_query=gitignore+file+explained+beginner)

### Practice

Create a `.gitignore` file and add suitable entries for your project.

Example:

```gitignore
node_modules/
dist/
.env
.DS_Store
```

Adjust the entries for the tools and files your project actually uses. Never commit passwords, API keys, tokens, or other secrets.

**Checkpoint:** You can prevent unnecessary or sensitive local files from being added to a repository.

---

## Step 6: Create a GitHub Repository and Connect Git

### Learn

- Creating a GitHub account
- Creating a repository on GitHub
- Cloning an existing repository
- Connecting a local repository to a remote
- `git remote`
- Pushing commits with `git push`
- Fetching and pulling updates

### Watch

- [GitHub Repositories, Clone, Push, and Pull](https://www.youtube.com/results?search_query=github+clone+push+pull+remote+beginner+tutorial)

### Practice

Clone a repository you own:

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
cd REPOSITORY
```

Replace the placeholders with your actual repository details.

If you already have a local repository that you want to connect to a new, empty GitHub repository, you can use:

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
git branch -M main
git push -u origin main
```

For an existing cloned repository, check `git remote -v` before adding another remote.

### Learn these commands

```bash
git remote -v
git fetch
git pull
git push
```

**Checkpoint:** You can move code between your local computer and GitHub.

---

## Step 7: Branches and Merging

### Learn

- Why branches are useful
- Creating a branch
- Switching branches
- Making commits on a branch
- Merging branches
- Resolving basic merge conflicts
- Deleting a branch after merging

### Watch

- [Git Branching and Merging for Beginners](https://www.youtube.com/results?search_query=git+branch+switch+merge+conflicts+beginner+tutorial)

### Practice

Create a feature branch:

```bash
git switch -c feature/add-about-page
```

Make a change, stage it, and commit it:

```bash
git add .
git commit -m "feat: add about page"
```

Return to the main branch and merge the feature branch:

```bash
git switch main
git merge feature/add-about-page
```

**Checkpoint:** You can work on a separate branch and integrate changes into another branch.

---

## Step 8: Pull Requests and Code Review

### Learn

- What a pull request (PR) is
- Why teams use pull requests
- Comparing branches
- Writing a clear PR title and description
- Reviewing another contributor's changes
- Requesting and responding to feedback
- Updating a branch after review

### Watch

- [GitHub Pull Requests and Code Review for Beginners](https://www.youtube.com/results?search_query=github+pull+requests+code+review+beginner+tutorial)

### Practice

1. Push a feature branch to GitHub.
2. Open the repository in your browser.
3. Create a pull request into the intended base branch.
4. Explain what you changed and how you tested it.
5. Review the changes in the PR before merging.

Example push command:

```bash
git push -u origin feature/add-about-page
```

**Checkpoint:** You can submit changes for review instead of directly changing the main branch.

---

## Step 9: Resolve Merge Conflicts

### Learn

- What causes a merge conflict
- Conflict markers such as `<<<<<<<`, `=======`, and `>>>>>>>`
- How to inspect conflicting changes
- How to choose or combine the correct changes
- How to mark conflicts resolved and finish the merge

### Watch

- [Git Merge Conflicts — Step-by-Step Tutorial](https://www.youtube.com/results?search_query=git+merge+conflicts+resolve+step+by+step+beginner)

### Practice

1. Create two branches from the same starting commit.
2. Change the same line in the same file on each branch.
3. Merge one branch into the other.
4. Open the conflicted file and inspect the markers.
5. Edit the file to keep the intended result.
6. Stage the resolved file and complete the merge.

```bash
git status
git add path/to/resolved-file
git commit
```

The final command applies to a normal merge conflict workflow; follow Git's instructions if you're resolving a conflict during a rebase or another operation.

**Checkpoint:** You can resolve a simple conflict without accidentally losing the intended changes.

---

## Step 10: Fork and Contribute to Open Source

### Learn

- Forking a repository
- Cloning your fork
- Keeping your fork synchronized with the original repository
- Finding beginner-friendly issues
- Reading `README.md` and `CONTRIBUTING.md`
- Following contribution guidelines
- Creating a branch and opening a PR
- Respectful communication and review etiquette

### Watch

- [How to Contribute to Open Source on GitHub](https://www.youtube.com/results?search_query=how+to+contribute+to+open+source+github+beginner+fork+pull+request)

### Practice

1. Choose a public repository with clear contribution instructions.
2. Read its README and contribution guidelines.
3. Find an issue appropriate for your skill level.
4. If the project asks contributors to claim or discuss an issue first, follow that process.
5. Fork the repository and clone your fork.
6. Create a new branch.
7. Make one focused change.
8. Test the change and commit it.
9. Push the branch and open a pull request.
10. Respond politely to feedback.

**Checkpoint:** You understand the typical open-source contribution workflow.

---

## Step 11: Useful GitHub Features

### Learn

- Issues and issue templates
- Discussions
- Labels and milestones
- README files and Markdown
- Releases and tags
- GitHub Actions at a basic level
- Repository permissions and branch protection
- Security alerts and secret handling

### Watch

- [GitHub Features for Developers](https://www.youtube.com/results?search_query=github+issues+discussions+actions+releases+beginner+tutorial)

### Practice

1. Create a clear README for one of your projects.
2. Open an issue describing a feature or bug.
3. Use Markdown headings, links, lists, and checkboxes.
4. Explore the Actions tab in a test repository.
5. Review the repository's security and access settings.

**Checkpoint:** You can navigate the key features used in collaborative repositories.

---

## Step 12: Build a Version-Controlled Project

Create a small project using the HTML, CSS, and JavaScript skills you've learned.

### Requirements

- A clear project README
- A `.gitignore` file appropriate to the project
- A Git repository with meaningful commit history
- At least one feature branch
- Descriptive commit messages
- A GitHub remote containing your work
- A short explanation of how to run the project
- No committed secrets or unnecessary generated files

### Suggested project

Build a simple personal portfolio page and use Git to track its development.

**Optional challenge:** Ask a friend to review your repository or open a pull request with an improvement.

**Checkpoint:** You can explain your commit history and demonstrate how you used branches to develop a feature.

---

## Recommended Learning Resources

- [Pro Git Book](https://git-scm.com/book/en/v2) — a comprehensive, free Git book.
- [Official Git Documentation](https://git-scm.com/doc) — commands and reference material.
- [GitHub Docs: Get Started](https://docs.github.com/en/get-started) — learn GitHub workflows.
- [GitHub Skills](https://skills.github.com/) — interactive, practical GitHub courses.
- [GitHub Docs: Contributing to Projects](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-a-project) — learn the contribution process.

---

## Final Completion Checklist

- [ ] Explain Git and GitHub in your own words.
- [ ] Install and configure Git.
- [ ] Initialize a repository and create commits.
- [ ] Inspect changes and review commit history.
- [ ] Use `.gitignore` appropriately.
- [ ] Clone a repository and push changes to GitHub.
- [ ] Create branches and merge changes.
- [ ] Open and review a pull request.
- [ ] Resolve a simple merge conflict.
- [ ] Follow a project's contribution guidelines.
- [ ] Make a small open-source contribution or complete a realistic practice PR.
- [ ] Publish a project with a useful README.

## What's Next?

Continue to [Frontend Development](05-frontend-development.md) to learn how to organize and build interactive user interfaces using modern frontend tools.

---

**Remember:** Git is more than a backup tool. It gives you a history of your work and helps you collaborate safely. Practice in a test repository before using unfamiliar commands on important projects.
