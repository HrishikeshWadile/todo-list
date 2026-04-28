Git-Based Source Code Management, Version Control & Build Management (15 Marks)
🔹 1. Initialize Repository & Push Flask Project
# Initialize Git repository
git init

# Add all Flask project files
git add .

# First commit
git commit -m "initial commit - flask app setup"

# Connect to GitHub repository
git remote add origin https://github.com/HrishikeshWadile/to-do-list

# Push code to GitHub
git branch -M main
git push -u origin main
🔹 2. Branching Workflow (Feature Development)
Create a new branch for feature work:
git branch feature-form
git checkout feature-form

OR shortcut:

git checkout -b feature-form
Make changes (example: form validation in Flask app)
git add .
git commit -m "added form validation logic"
🔹 3. Merge Branch into Main
# Switch back to main branch
git checkout main

# Merge feature branch
git merge feature-form

If no conflicts → merge completes successfully.

🔹 4. Handle Merge Conflicts (if any)

If conflict occurs:

Open conflicting file
Resolve manually
Then:
git add .
git commit -m "resolved merge conflict between main and feature-form"
🔹 5. Track Commit History
git log

Optional cleaner view:

git log --oneline

This shows:

Commit IDs
Messages
Branch history
🔹 6. Revert Changes (Rollback Feature)

If a bug is introduced:

git revert <commit-id>

Example:

git revert a3f5c21

This creates a new commit that undoes changes safely.

🔹 7. Collaboration Workflow (GitHub-Based)

Typical workflow used in team development:

Clone repository:
git clone https://github.com/your-username/flask-app.git
Create feature branch:
git checkout -b ui-updates
Work + commit changes:
git add .
git commit -m "improved UI layout"
Push branch:
git push origin ui-updates
Create Pull Request (GitHub)
Review → Merge into main branch
🔹 8. Build Version Tracking

To identify versions used in build:

git tag v1.0
git push origin v1.0

Check deployed version:

git show v1.0

Or track exact commit used for deployment:

git rev-parse HEAD
🔹 Expected Outcome
Flask application managed using GitHub repository
Proper branching and merging workflow
Commit history tracking for all changes
Conflict resolution handled manually
Ability to rollback using revert
Version tagging for builds and releases
Demonstrates full collaboration workflow in software development