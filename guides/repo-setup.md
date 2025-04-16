---
layout: default
title: Repository Setup
nav_order: 2
parent: Guides
has_children: false
permalink: /repo-setup/
---

# Repository Setup
{: .no_toc }

This guide will walk you through setting up a GitHub repository for your project. This is a crucial step in the course, as it will allow you to collaborate with your team and track changes to your code.
Following these steps will ensure you have a well-structured repository that meets the course requirements.

<details open markdown="block">
  <summary>Table of Contents</summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

### Create a new repository
- Go to the GitHub Classroom page and accept an assignment `Course Project`.
- Create a new team with the name of your project (e.g., `Finance Flow`).
- Create a new repository with the name of your project (e.g., `finance-flow`).

### Clone the repository
- Clone the repository to your local machine using the following command:
```bash
git clone <repository-url>
```

### Create a new branch
- Create a new branch for your project using the following command:
```bash
git checkout -b <branch-name>
```
- Replace `<branch-name>` with a descriptive name for your branch (e.g., `feature/initial-setup`).
- This branch will be used for all your changes and commits required ti setup the repository.
- Make sure to commit your changes regularly and push them to the remote repository.
- Use the following command to push your changes:
```bash
git push origin <branch-name>
```
- Replace `<branch-name>` with the name of your branch.
- This will push your changes to the remote repository and create a new branch with the same name.
- You can also use the following command to push your changes:
```bash
git push -u origin <branch-name>
```
- This will set the upstream branch for your local branch to the remote branch, so you can use `git push` and `git pull` without specifying the branch name.
- This is useful if you are working on multiple branches and want to keep track of them easily.

### Create repository structure
- Create the following directory structure in your repository:
```
finance-flow/
├── .github/
│   ├── workflows/
│   └── issue_template/
├── docs/
├── src/
├── tests/
├── .gitignore
├── README.md
└── LICENSE
```
- The `.github` directory will contain the GitHub Actions workflows and issue templates.
- The `docs` directory will contain the documentation for your project.
- The `src` directory will contain the source code for your project.
- The `tests` directory will contain the test cases for your project.
- The `.gitignore` file will contain the files and directories that should be ignored by Git.
- The `README.md` file will contain the documentation for your project.
- The `LICENSE` file will contain the license for your project.

You can create the directories and files using the following commands:
```bash
mkdir -p .github/{workflows,issue_template}
mkdir -p {docs,src,tests}
touch .gitignore README.md LICENSE
```

### Create a README file
- The `README.md` file should contain the following information:
    - Project title
    - Project description
    - Installation instructions
    - Usage instructions
    - Contributing guidelines
    - License information

- You can use the following template for your `README.md` file:

### Create a .gitignore file
- The `.gitignore` file should contain the files and directories that should be ignored by Git.
- You can use the following template for your `.gitignore` file:
```
# IDE files
# Language specific files
# OS specific files
# Environment files
# Build files
# Test files
# Coverage files
# Logs
# Temporary files
# Backup files
# Database files
# Cache files
# Secrets
# Configuration files
```

### Create a LICENSE file
- The `LICENSE` file should contain the license for your project.
- You can use any open source license that you prefer.
- For example, you can use the MIT license, Apache 2.0 license, or GNU General Public License (GPL).

### Create a `.github/workflows` directory
- The `.github/workflows` directory will contain the GitHub Actions workflows for your project.

### Create a `.github/issue_template` directory
- The `.github/issue_template` directory will contain the issue templates for your project.
- You can create the following issue templates:
    - Bug report
    - Feature
    - ADR (Architectural Decision Record), you will need them later in the course
    - Task