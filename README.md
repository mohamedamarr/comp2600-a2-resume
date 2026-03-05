# Mohamed Kmr - 7951350
# COMP 2600 - Assignment 2 - Professor Tristan Miller — Hosting a Resume Website using Markdown, Jekyll, Git, and GitHub Pages

## Purpose

This README explains how to create and host a resume website using Markdown, Git, the Jekyll static site generator, and GitHub Pages. It serves two goals:

1. **A plain-language tutorial** that explains how a beginner can reproduce the workflow: write a resume in Markdown, convert it into a website using Jekyll, and publish it using GitHub Pages.

2. **A technical writing artifact** that explains *why* these tools were chosen and how they align with Andrew Etter’s *Modern Technical Writing* approach: lightweight formats, version control, and automated publishing.

The intended audience is Marvin McLaren, a finance manager who is learning about technical documentation tools. Marvin understands basic Markdown and simple command‑line commands, but he has no experience with Git, static site generators, or code forges such as GitHub. For that reason, these instructions are written clearly and sequentially so that someone with minimal technical experience can follow them.

The process described in this document follows principles from Andrew Etter’s *Modern Technical Writing*. Etter recommends using lightweight documentation tools that are easy to maintain, version, and publish. Markdown, Git, and static site generators follow this philosophy because they simplify documentation workflows and allow automation to handle formatting and deployment.

The final website contains:
- A **home page** (`index.markdown`) with a link to the resume.
- A **resume page** (`resume.md`) written in Markdown and rendered to HTML by Jekyll.



## Prerequisites

Before starting, make sure the following tools and resources are available.

### Required software

- A computer with macOS, Linux, or Windows
- A terminal or command prompt
- Git installed
- Ruby installed
- Bundler installed
- Jekyll installed
- A GitHub account

### Required knowledge

The reader should be able to:

- Navigate folders using the command line
- Create and edit Markdown files
- Run simple terminal commands

Using simple tools follows Etter’s recommendation to prefer systems that are easy to maintain, widely supported, and simple to automate.

---

## Instructions: Creating and Hosting the Resume Website

Follow the steps below in order. Each step contains **one clear action**, following the instruction‑writing guidelines for technical documentation.

---
To make the instructions usable:
- Each section is organized with clear headings.
- Steps are written in a predictable order.
- Commands are presented in copy-paste blocks.
- Explanations use plain language and define terms once before using them.

This matches Etter’s idea that documentation should be **easy to maintain**, **easy to publish**, and **usable by real readers**, not written like a textbook.

---


### Step 1: Create a GitHub repository

Open GitHub and create a new repository.

1. Log in to GitHub.
2. Click **New Repository**.
3. Enter a repository name (example: `comp2600-a2-resume`).
4. Set the repository to **Public**.
5. Click **Create Repository**.

Hosting the project on a forge such as GitHub allows documentation to be version controlled and published automatically. Etter emphasizes that documentation should live alongside the tools used to manage it.

---

### Step 2: Create a project folder

Open the terminal and create a folder for the project.

```bash
mkdir comp2600-a2-resume
cd comp2600-a2-resume
```

Initialize Git inside the folder.

```bash
git init
```

Version control is important because it records every change made to the documentation.

---

### Step 3: Install the Jekyll static site generator

Install Jekyll and Bundler using Ruby.

```bash
gem install jekyll bundler
```

Create the Jekyll website structure.

```bash
jekyll new .
```

Jekyll generates a folder structure that converts Markdown documents into HTML pages. Static site generators separate content from design, which supports maintainable documentation workflows.

---

### Step 4: Create the resume in Markdown

Create a file named:

```
resume.md
```

Write the resume using Markdown formatting.

Example:

```markdown
# Mohamed Wael Kmr

## Education
University of Manitoba — Computer Science

## Experience
Server – Rae & Jerry’s Steakhouse

## Skills
Leadership  
Customer Service  
Team Collaboration
```

Markdown is preferred over complex formatting systems because it allows writers to focus on the content rather than presentation.
It is a lightweight way to write structured text (headings, lists, emphasis) without fighting formatting tools.

---

### Step 5: Add the resume to the homepage

Open the file:

```
index.markdown
```

Add a link to the resume.

```markdown
## Welcome

Welcome to my resume website.

[View My Resume](resume)
```

This step ensures that visitors can easily find the resume from the main page.

---

### Step 6: Test the website locally

Run the local Jekyll server.

```bash
bundle exec jekyll serve
```

Open a browser and visit:

```
http://127.0.0.1:4000
```

Testing the website locally allows you to confirm that the pages render correctly before publishing them online.

---

### Step 7: Commit the files

Add all files to Git.

```bash
git add .
```

Create a commit.

```bash
git commit -m "Initial resume website"
```

Git records each version of the project, allowing changes to be tracked over time.

---

### Step 8: Connect the repository to GitHub

Link the local project to the GitHub repository.

```bash
git remote add origin https://github.com/USERNAME/comp2600-a2-resume.git
```

Push the files to GitHub.

```bash
git push -u origin main
```

After pushing, the repository becomes available online.

---

### Step 9: Enable GitHub Pages

Open the repository on GitHub.

1. Click **Settings**.
2. Click **Pages**.
3. Select the **main branch** as the source.
4. Save the configuration.

After deployment completes, the website will appear at:

https://USERNAME.github.io/comp2600-a2-resume/

* Example:

https://mohamedamarr.github.io/comp2600-a2-resume/

Automated publishing is a major advantage of static site workflows because it reduces manual steps.

---
### How this assignment supports Andrew Etter’s principles that good technical documentation should be:
* Markdown keeps documentation lightweight and readable, making it easy to write and maintain.
* Git stores a clear history of changes, allowing documentation to be version-controlled like software.
* GitHub Pages publishes the site automatically, removing the need for manual deployment.



Jekyll generates consistent output without manual formatting work.
GitHub Pages automates publishing so the “source of truth” is always the repository. 

## Further Resources

* Markdown Guide  
[Markdown Guide](https://www.markdownguide.org/)

* Jekyll Documentation  
[Jekyll Documentation](https://jekyllrb.com/docs/)

* Git Documentation  
[Git Documentation](https://git-scm.com/docs)

* GitHub Pages Documentation  
[GitHub Pages Documentation](https://docs.github.com/en/pages)

* Andrew Etter, Modern Technical Writing (documentation principles: lightweight tools, docs-as-code, automation).

---

## FAQ

### Why use Markdown instead of writing HTML?

Markdown is easier to read and write than HTML. It allows documentation to remain clean and simple while still producing properly formatted web pages when processed by a static site generator.

### Why don't my changes appear on the website immediately?

When using GitHub Pages, the site is rebuilt after each commit. This process can take a few minutes. Refreshing the page after the build completes should show the updates.

---
## Credits

Author: Mohamed Wael Kmr  
Course: COMP 2600 – Technical Communication in Computer Science

Website generated using **Jekyll**.

Hosting provided by **GitHub Pages**.

Helpful resources include the Markdown Guide, Jekyll documentation, Git documentation, and GitHub Pages documentation.
