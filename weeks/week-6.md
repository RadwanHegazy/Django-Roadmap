# Week 6: Git & GitHub

Version control is essential for modern software development. This week covers Git, the most popular version control system, and GitHub, the platform for hosting and collaborating on Git repositories. You'll learn to track changes, collaborate with others, and manage your codebase effectively.

## Topics Covered

1. **Git Basics**
   - What is version control?
   - Installing Git
   - Initializing a repository
   - Basic Git workflow (add, commit, push, pull)

2. **Git Commands**
   - git status, git log, git diff
   - Branching and merging
   - Resolving merge conflicts
   - Undoing changes (reset, revert, checkout)

3. **GitHub**
   - Creating repositories
   - Cloning repositories
   - Forking and pull requests
   - GitHub issues and project boards

4. **Collaboration Workflow**
   - Working with teams
   - Code reviews
   - Branching strategies (Git Flow, GitHub Flow)

5. **Markdown**
   - Basic Markdown syntax
   - Writing README files
   - Documentation best practices

6. **Commit Messages**
   - Writing good commit messages
   - Conventional commits
   - Commit message standards

7. **.gitignore**
   - What to ignore
   - Creating .gitignore files
   - Global vs local .gitignore

## Resources

- [Arabic GitHub Crash Course](https://www.youtube.com/watch?v=Q6G-J54vgKc)
- [Markdown Tutorial](https://www.youtube.com/watch?v=_PPWWRV6gbA)
- [Commit Messages Guide](https://www.youtube.com/watch?v=XMqPHAq4xkQ)
- [.gitignore Tutorial](https://www.youtube.com/watch?v=3dnC85b7CTQ)

## Tasks

### Task 1: Git Setup and Basic Commands
Set up Git and practice basic version control operations.

**Requirements:**
- Install Git on your system
- Configure Git with your name and email
- Create a local repository
- Practice add, commit, and log commands
- Create and switch between branches

**Basic Commands:**
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git init
git add .
git commit -m "Initial commit"
git log --oneline
git branch feature-branch
git checkout feature-branch
```

### Task 2: GitHub Repository Setup
Create and manage a GitHub repository for your Django project.

**Requirements:**
- Create a GitHub account (if you don't have one)
- Create a new repository
- Push your local Django project to GitHub
- Set up a README.md file
- Add a .gitignore file for Python/Django

**Example .gitignore for Django:**
```
# Byte-compiled / optimized / DLL files
__pycache__/
*.py[cod]
*$py.class

# Django
*.log
local_settings.py
db.sqlite3
db.sqlite3-journal

# Environment variables
.env

# Virtual environments
venv/
env/
ENV/

# IDE
.vscode/
.idea/
```

### Task 3: Branching and Merging
Practice branching workflow and conflict resolution.

**Requirements:**
- Create feature branches for new functionality
- Make changes on different branches
- Merge branches back to main
- Resolve merge conflicts (create intentional conflicts to practice)
- Use git merge vs git rebase

### Task 4: Collaboration Simulation
Simulate collaborating with other developers.

**Requirements:**
- Fork a repository (or create a second local repo)
- Make changes and create a pull request
- Review and merge pull requests
- Practice code review process
- Use GitHub issues for task tracking

### Task 5: Documentation with Markdown
Create comprehensive documentation for your Django project.

**Requirements:**
- Write a detailed README.md for your Django project
- Include sections: Description, Installation, Usage, Contributing
- Use proper Markdown formatting
- Add badges, screenshots, or GIFs if possible

**Example README Structure:**
```markdown
# Project Name

Brief description of your Django project.

## Features

- Feature 1
- Feature 2
- Feature 3

## Installation

1. Clone the repository
2. Install dependencies
3. Run migrations
4. Start the server

## Usage

Describe how to use your application.

## Contributing

Guidelines for contributing to the project.
```

## Tips for Success

- Commit early and often with descriptive messages
- Use branches for new features or experiments
- Always pull before pushing to avoid conflicts
- Learn keyboard shortcuts for your Git GUI client
- Practice the Git workflow until it becomes second nature
- Use GitHub's web interface for simple operations

## Next Steps

Git and GitHub skills are crucial for any development career. In Week 7, we'll explore networking fundamentals, which will help you understand how web applications communicate. Meanwhile, continue practicing Git by versioning all your future projects.

Remember: Git is your safety net – it allows you to experiment fearlessly! 🔄
