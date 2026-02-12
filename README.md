# Git & GitHub Learning Repository

This repository documents our group’s learning journey while auditing Google’s
“Introduction to Git and GitHub” course on Coursera.

The goal of this repository is to demonstrate practical understanding of Git,
GitHub, and collaborative workflows through consistent commits, structured notes,
and hands-on exercises aligned with each course module.

## Contributors
- Absolom Orianga
- Travis Mark Lufene
- Mubiru Humphery
- Puoch Mabor Makuei
- Sebatta Allan Kagimu

## Repository Structure
The repository is organized in course modules. Each module contains folders for
individual contributors as well as shared demonstration files where applicable.

## Collaboration Workflow
- **Modules 1–2:** Direct commits to `main` within individual folders.
- **Module 3:** Introduction of remote repositories and occasional branching.
- **Module 4:** Branch-based development using pull requests, code reviews, and
  controlled merges into `main`.

This workflow evolves to mirror the concepts taught in the course.

**Module 1-2**
1. The "Sandbox" Structure (Individual Folders)
To allow 30+ students to commit simultaneously without catastrophic merge conflicts, the repository is structured with rigid isolation.

The Rule: Each student is assigned a specific directory (e.g., /Module1/StudentName/ or /Assignments/StudentID/).

The Boundary: Students are instructed never to touch files outside their folder.

The Implication: Because file paths don't intersect, Git treats the changes as independent. Two students can commit at the same time without creating conflicts.

2. The "Main" Branch Mentality
During Modules 1–2, students operate under the Centralized Workflow (even if they don't know the term yet).

No Branches: All work is performed on the main branch (or master).

Direct Commits: There are no Pull Requests. There is no code review. Students commit directly to main after staging (git add) and committing (git commit -m).

The PUSH: At the end of the session, students run git pull (to get everyone else’s folders) and git push to upload their own folder.

3. The Learning Objectives
In Modules 1–2, the instructor is not teaching collaboration; they are teaching version control and local repository management.

Key Concepts Covered:

Staging vs. Committing: Understanding that git add puts files in the "staging area" and git commit saves them to history.

Writing Commit Messages: Learning to write clear messages, even if they are currently single-user.

Viewing History: Using git log to see the timeline of changes (including classmates' commits in other folders).

The Three States: Modified, Staged, Committed.

4. The "Easy" Conflicts
Because students work in separate folders, merge conflicts are rare. However, they occasionally occur if:

A student forgets to pull before push (resulting in a non-fast-forward error).

A student accidentally edits the README or a course-wide config file.

Resolution Strategy (Module 1-2 style): Since there are no branches, the resolution is usually a simple git pull --no-ff or forcing the student to re-commit after updating their local copy.
