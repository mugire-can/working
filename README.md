# Working Project

A professional project repository for development and collaboration with multiple development phases.

## Overview

This project demonstrates a complete Git workflow with multiple working branches for different development phases, feature implementations, and PR-based merging strategy.

## Branches

- **main** - Production-ready code (HEAD)
- **Working-01** - First development phase (setup & configurations)
- **Working-02** - Second development phase (modifications from Linux environment)
- **Working-03** - Third development phase (.gitignore & README.md files)
- **Working-04** - Fourth development phase

## Getting Started

### Prerequisites

- Git installed on your system
- Basic knowledge of Git workflow
- Node.js (optional, for JavaScript projects)
- Python 3.x (optional, for Python projects)

### Clone the Repository

```bash
git clone https://github.com/mugire-can/working.git
cd working
```

### Switch Between Branches

```bash
git checkout <branch-name>
git checkout Working-01
```

### Create a New Branch

```bash
git checkout -b <new-branch-name>
git checkout -b Working-05
```

## Git Workflow

### Making Changes

1. Create or switch to your working branch
   ```bash
   git checkout -b feature-branch
   ```

2. Make your changes to files

3. Stage changes
   ```bash
   git add .
   git add <specific-file>
   ```

4. Commit changes
   ```bash
   git commit -m "Descriptive commit message"
   ```

5. Push to remote
   ```bash
   git push origin <branch-name>
   git push -u origin feature-branch
   ```

### Creating a Pull Request

1. Push your branch to GitHub
   ```bash
   git push origin <branch-name>
   ```

2. Go to GitHub and create a Pull Request
3. Add description and request reviewers
4. Wait for reviews and approval

### Merging to Main

**Via Pull Request (Recommended):**
1. Create PR on GitHub
2. Get approval from reviewers
3. Click "Merge" button on GitHub
4. Pull latest locally
   ```bash
   git checkout main
   git pull origin main
   ```

**Via Command Line:**
```bash
git checkout main
git pull origin main
git merge <branch-name>
git push origin main
```

## Project Structure

```
working/
├── .git/                 # Git repository metadata
├── .gitignore           # Git ignore rules
├── README.md            # This file
├── working-1.txt        # Initial project file
└── [other project files]
```

## Version History

### Recent Commits
- **Working-04 started** (Dec 17, 11:52 AM) - Fourth phase initiated
- **Working-04 Merge PR #2** (Dec 17, 11:54 AM) - Merged via GitHub PR
- **Working-03 Merge PR #1** (Dec 17, 11:46 AM) - Added .gitignore & README.md
- **Working-02 modified** (Dec 17, 10:56 AM) - Linux system modifications
- **Working-02 started** (Dec 17, 10:44 AM) - Second phase started
- **Working started** (Dec 17, 10:30 AM) - Initial project commit

## Best Practices

1. **Always pull before pushing**
   ```bash
   git pull origin main
   ```

2. **Use meaningful commit messages**
   ```bash
   # Good
   git commit -m "Add user authentication feature"
   
   # Avoid
   git commit -m "fix stuff"
   ```

3. **Create branches for new features**
   ```bash
   git checkout -b feature/new-feature
   ```

4. **Never force push to main**
   ```bash
   # Don't do this on main!
   git push --force origin main
   ```

5. **Review your changes before committing**
   ```bash
   git diff
   git status
   ```

## Common Commands Reference

```bash
# View status
git status

# View changes
git diff
git diff --cached

# View history
git log
git log --oneline
git log --graph --all --decorate

# Undo changes
git checkout -- <file>
git restore <file>

# Stash changes
git stash
git stash pop

# Rebase
git rebase main

# Cherry-pick commits
git cherry-pick <commit-sha>
```

## Troubleshooting

### Merge Conflicts
When conflicts occur:
```bash
git status                    # See conflicted files
# Edit files to resolve conflicts
git add <resolved-files>
git commit -m "Resolve merge conflicts"
```

### Undo Last Commit (not pushed)
```bash
git reset --soft HEAD~1
```

### Undo Last Commit (already pushed)
```bash
git revert HEAD
git push origin main
```

## Contributing

1. Create a new branch from main
2. Make your changes
3. Commit with clear messages
4. Push to remote
5. Create a Pull Request
6. Wait for approval and merge

## Author

**mugire-can** - [GitHub Profile](https://github.com/mugire-can)

## Repository

[https://github.com/mugire-can/working](https://github.com/mugire-can/working)

## License

All rights reserved.

## Notes

- All changes are tracked in Git
- Use descriptive branch names
- Review changes before merging to main
- Keep commits focused and atomic
- Update README.md when adding significant features
