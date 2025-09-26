## Task 4 Documentation

# DevOps Git Demo Project - Task Steps

## 1. Project Initialization
- Created project directory:
```bash
mkdir devops-git-demo
cd devops-git-demo
Initialized Git repository:

git init
Created initial README.md:
echo "# DevOps Git Demo Project" > README.md
git add .
git commit -m "Initial commit: setup project"

**## 2. Connect to GitHub**
Added remote repository: git remote add origin https://github.com/<your-username>/devops-git-demo.git
Renamed branch to main: git branch -M main
Pushed initial commit: git push -u origin main

**3. Branch Creation**
Created development branch:

git checkout -b dev
git push origin dev
Created feature branch for CI/CD:

git checkout -b feature/add-ci-pipeline
git push origin feature/add-ci-pipeline

**4. Development on Feature Branch**
Created a placeholder file for CI/CD pipeline:

echo "CI/CD pipeline placeholder" > pipeline.yml
git add pipeline.yml
git commit -m "Add: initial CI/CD pipeline file"
git push origin feature/add-ci-pipeline

**5. Pull Request Workflow**
Opened PR from feature/add-ci-pipeline → dev on GitHub

Conducted code review and merged PR into dev

Merged dev → main when stable and production-ready

**6. .gitignore**
Created .gitignore file to ignore unnecessary files:
__pycache__/
*.pyc
node_modules/
*.log


git add .gitignore
git commit -m "Add .gitignore file"
git push origin dev

7. Tagging Releases
Created Git tag for versioning:
git tag v1.0
git push origin v1.0

8. Documentation
Created docs/ directory and added task documentation:
mkdir docs
echo "## Task 4 Documentation" > docs/TASKS.md
git add docs/TASKS.md
git commit -m "Docs: add task documentation"
git push origin dev

**9. Workflow Diagram (ASCII)**

feature/add-ci-pipeline  -->  dev  -->  main
        |                   ^
        |                   |
      PR merge            PR merge

**For hotfix:**
hotfix/fix-bug  -->  main
        |
        v
      dev merge

**10. Commands Summary**
Action	Command
Initialize repo	git init
Add remote	git remote add origin <url>
Commit changes	git add .
git commit -m "message"
Push branch	git push origin <branch>
Create branch	git checkout -b <branch>
Merge branch	PR on GitHub / git merge <branch>
Tag release	git tag v1.0
git push origin v1.0
Stash changes	git stash / git stash pop
Ignore files	.gitignore

**11. Learning Outcome**
Learned Git best practices for DevOps.

Practiced branching, pull requests, merge strategies.

Learned to maintain a clean repo with .gitignore and tags.

Documented workflow and commands using Markdown.
