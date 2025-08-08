# Git Branching Workflow Tasks

This document outlines the tasks and steps for maintaining the Git branching workflow.

---

## 1️⃣ Initial Setup
- [x] Create `main` branch (default)
- [x] Create `dev` branch from `main`
  ```bash
  git checkout main
  git checkout -b dev
  git push -u origin dev
  
2️⃣ Feature Development
 Create a new branch from dev

git checkout dev
git checkout -b feature/login
git push -u origin feature/login
 Implement new feature

 Commit changes with descriptive messages

 Push feature branch to remote

3️⃣ Code Review & Merge
 Open Pull Request (PR) from feature/* → dev

 Review code

 Merge after approval

4️⃣ Pre-Production Merge
 Test all features in dev

 Open PR from dev → main

 Merge after successful testing

5️⃣ Cleanup
 Delete merged feature branches locally and remotely if you want

git branch -d feature/login
git push origin --delete feature/login

🔄 Repeat Process
For each new feature