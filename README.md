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
The repository is organized by course modules. Each contributor works on a
personal branch, committing lecture summaries and any complementary code
samples, then merges changes into `main` via pull requests.

## Collaboration Workflow
Each contributor works on their own branch and submits pull requests to merge
into `main`. We do not commit directly to `main`, and we do not use individual
folders that commit to `main`.


## This workflow mirrors the course’s branch-based collaboration model.##
This workflow mirrors the course’s branch-based collaboration model.
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

This workflow evolves to mirror the concepts taught in the course.

## Module 1-2
**1.The "Sandbox" Structure (Individual Folders)**


To allow 30+ students to commit simultaneously without catastrophic merge conflicts, the repository is structured with rigid isolation.

The Rule: Each student is assigned a specific directory (e.g., /Module1/StudentName/ or /Assignments/StudentID/).

The Boundary: Students are instructed never to touch files outside their folder.

The Implication: Because file paths don't intersect, Git treats the changes as independent. Two students can commit at the same time without creating conflicts.

**2. The "Main" Branch Mentality**


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

**4. The "Easy" Conflicts**


Because students work in separate folders, merge conflicts are rare. However, they occasionally occur if:

A student forgets to pull before push (resulting in a non-fast-forward error).

A student accidentally edits the README or a course-wide config file.

**Module 3**
1. The Cognitive Shift: Local vs. Remote
In Modules 1-2, students thought of Git as a tool on their hard drive. In Module 3, the concept of the Remote (usually GitHub/GitLab) becomes a first-class citizen.

Origin is Introduced: Students learn that origin is just a nickname for the URL of the server.

Fetch vs. Pull: Instructors introduce git fetch to "check" what has changed on the server without merging it, teaching students to inspect changes before integrating them.

Cloning: Instead of starting a repository with init, students learn to start by copying an existing one with git clone.

2. The Introduction of "Occasional" Branching
This is the most significant technical leap in Module 3. Students are no longer tied to the main trunk.

Why Branch? Instructors introduce the concept of a "sandbox" or "experiment." If a student wants to try a risky change (refactoring code, testing a new library), they can do it on a branch without breaking the working version on main.

Basic Branch Commands: Students learn git branch <name>, git switch <name> (or checkout), and the crucial step of merging a branch back into main locally.

The "Occasional" Nature: At this stage, branching is usually for personal experimentation or specific assignment checkpoints, rather than the default method of work. It might be used to separate "Part A" of an assignment from "Part B."

3. The Collaboration Style: "Asynchronous Handoff"
Collaboration in Module 3 is more intentional than in Modules 1-2, but still less formal than Pull Requests.

Working on the Same File (Finally): Because of branching, students can now theoretically work on the same file without immediate disaster. If Student A branches to edit readme.md and Student B stays on main to edit it, they will eventually have to reconcile.

The Remote as Hub: Students are taught that the Remote repository is the "source of truth" and the medium for sharing work. "Hey, I finished my part, I pushed it to a branch called feature-login, you can check it out."

Conflict Resolution Deep Dive: Because branching invites parallel edits, Module 3 is usually where real merge conflicts are taught. Students learn to read the <<<<<<< HEAD markers and decide which code to keep.

4. The Workflow in Practice (Example)
A typical Module 3 assignment might look like this:

Clone: Student clones the class repo (or a partner repo) from GitHub.

Branch: Student creates a branch called feature-calculator to build a new function.

Commit (Local): They commit multiple times on their branch.

Publish Branch: The student pushes the branch to the remote (git push origin feature-calculator).

Partner Interaction: The partner fetches the remote branches (git fetch) and checks out that branch to look at the code, or merges it into their own branch to test integration.

Local Merge: Once the feature works, the student switches back to main and merges feature-calculator into their local main.

Push: The student pushes the updated main to the remote.

Resolution Strategy (Module 1-2 style): Since there are no branches, the resolution is usually a simple git pull --no-ff or forcing the student to re-commit after updating their local copy.
====
For merge conflicts involving `README.md`, use the `Puoch-Mabor-M` branch version as the authoritative source.
