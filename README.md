# Git & GitHub Collaborative Learning Repository

## Overview
This repository documents our group’s learning journey while studying Git and GitHub through both the **Google "Introduction to Git and GitHub" Coursera course** and the **W3Schools Git Tutorial**.

The repository serves as a practical workspace where we apply version control concepts through structured notes, exercises, and collaborative development workflows.

## Purpose
This repository is used to:

- Demonstrate practical understanding of Git and GitHub concepts  
- Practice real-world collaborative development workflows  
- Track individual and group contributions through commits and pull requests  
- Document lecture summaries, exercises, and learning reflections  
- Build confidence using distributed version control systems  

## Contributors
- Absolom Orianga  
- Travis Mark Lufene  
- Mubiru Humphery  
- Puoch Mabor Makuei  
- Sebatta Allan Kagimu  

## Repository Structure
The repository is organized according to learning modules and exercises from both learning platforms. Each module contains folders for individual contributors and shared demonstration files where applicable. Contributors submit:

- Lecture and tutorial summaries  
- Practical exercises  
- Supporting code samples where applicable  
- Notes and documentation related to Git concepts  

## Collaboration Workflow
To encourage proper version control practices and transparency in contribution tracking:

- Each contributor works on their **own branch**
- Work is committed regularly with clear commit messages
- Changes are submitted through **Pull Requests**
- Pull Requests are reviewed before merging into `main`
- Direct commits to `main` are avoided to maintain repository stability

This workflow mirrors industry-standard collaborative development practices and the concepts taught in the course.

### How code reviews improve software quality and developer skills
Code reviews allow developers to examine each other’s work before it becomes part of the main project. This helps detect bugs, security issues, and inefficient logic early, improving overall software quality. At the same time, developers learn new techniques, coding standards, and best practices from feedback. Junior developers gain mentorship, while experienced developers refine their communication and design thinking skills.

## Tools and Platforms Used
- Git  
- GitHub  
- Google Coursera – Introduction to Git and GitHub  
- W3Schools Git Tutorial  
- Code Editors (e.g., Visual Studio Code)

## Learning Outcome
By completing both learning platforms and practicing collaboratively in this repository, the group aims to:

- Understand Git architecture and workflows  
- Apply branching and merging strategies effectively  
- Use GitHub collaboration tools such as pull requests and reviews  
- Develop industry-ready version control skills  
- Strengthen teamwork and collaborative software development practices  

## Notes
This repository functions as a shared learning log and collaborative workspace where progress, participation, and understanding of Git concepts can be clearly demonstrated.

<<<<
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
