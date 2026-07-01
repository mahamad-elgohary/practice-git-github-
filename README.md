# Git Mastery Lab – 25 Scenario Challenge

## Overview

This project is a hands-on Git training laboratory designed to develop a deep understanding of Git internals, workflows, history manipulation, recovery techniques, branching strategies, merging, rebasing, stashing, and disaster recovery.

The goal is not merely to memorize commands, but to understand how Git manages:

* Working Tree
* Staging Area (Index)
* Local Repository
* Branch Pointers
* HEAD
* Remote References
* Commit Graphs
* Reflog Entries

By the end of this lab, you should be able to diagnose and recover from common and advanced Git mistakes without relying on a graphical interface.

---

# Learning Objectives

After completing all scenarios, you should be able to:

* Track and untrack files correctly.
* Manage the staging area confidently.
* Create meaningful commits.
* Recover from accidental resets.
* Understand branch pointers and HEAD behavior.
* Work with detached HEAD states safely.
* Merge branches and resolve conflicts.
* Revert normal and merge commits.
* Use stashes effectively.
* Rebase branches and rewrite history.
* Perform interactive rebases.
* Recover seemingly lost commits using reflog.
* Explain how Git stores and references history.

---

# Repository Setup

Create the repository:

```bash
mkdir OS-KnowledgeBase
cd OS-KnowledgeBase
git init
```

Suggested structure:

```text
OS-KnowledgeBase/
│
├── README.md
├── notes/
│   ├── processes.txt
│   ├── memory.txt
│   └── scheduling.txt
│
├── algorithms/
│   ├── sorting.txt
│   └── searching.txt
│
└── networking/
    ├── tcp.txt
    └── udp.txt
```

---

# Rules

For every scenario:

1. Predict the outcome before executing commands.
2. Draw the commit graph.
3. Identify:

   * Current Branch
   * HEAD Position
   * Working Tree State
   * Staging Area State
4. Execute commands.
5. Verify results using:

```bash
git status
git log --oneline --graph --all
git reflog
```

6. Document:

   * Expected Result
   * Actual Result
   * Lessons Learned

---

# Phase 1 – Tracking & Staging

## Scenario 1

Track only selected files and analyze Git status.

## Scenario 2

Use staging and unstaging operations correctly.

## Scenario 3

Partially unstage files after accidental staging.

## Scenario 4

Work with a mixture of staged and unstaged modifications.

## Scenario 5

Configure and verify `.gitignore` behavior.

---

# Phase 2 – Commit Manipulation

## Scenario 6

Amend an existing commit.

## Scenario 7

Create and analyze a commit history chain.

## Scenario 8

Use `git reset --soft`.

## Scenario 9

Use `git reset --mixed`.

## Scenario 10

Use `git reset --hard` and recover using reflog.

---

# Phase 3 – Branch Management

## Scenario 11

Create branches and verify pointer movement.

## Scenario 12

Safe delete vs force delete branches.

## Scenario 13

Rename and organize branches.

## Scenario 14

Create and recover detached HEAD commits.

---

# Phase 4 – Merge Operations

## Scenario 15

Perform a successful merge.

## Scenario 16

Create and resolve merge conflicts.

## Scenario 17

Revert a merge using:

```bash
git revert -m 1
```

## Scenario 18

Analyze:

```bash
git revert -m 2
```

and compare results.

---

# Phase 5 – Stash Management

## Scenario 19

Stash mixed staged and unstaged changes.

## Scenario 20

Manage multiple stashes.

## Scenario 21

Switch branches safely using stash workflows.

---

# Phase 6 – Rebasing

## Scenario 22

Perform a standard branch rebase.

## Scenario 23

Interactive rebase:

* squash
* drop
* rename commits

## Scenario 24

Interactive rebase with edit and amend.

---

# Phase 7 – Disaster Recovery

## Scenario 25 – Final Boss

Simulate repository corruption involving:

* Hard resets
* Branch deletion
* Detached HEAD commits
* Bad rebases

Recover the repository using:

```bash
git reflog
git branch
git checkout
git reset
```

without using any GUI tools.

---

# Deliverables

For every scenario maintain:

```text
Scenario-X/
│
├── commands.txt
├── predictions.txt
├── observations.txt
└── lessons-learned.txt
```

Each folder should contain:

* Commands executed
* Predicted outcomes
* Actual outcomes
* Graph sketches
* Recovery steps (if applicable)

---

# Recommended Verification Commands

Check status:

```bash
git status
```

Visualize history:

```bash
git log --oneline --graph --decorate --all
```

Inspect branches:

```bash
git branch -av
```

Inspect remotes:

```bash
git remote -v
```

Inspect reflog:

```bash
git reflog
```

Inspect stashes:

```bash
git stash list
```

---

# Graduation Requirements

You have successfully completed the Git Mastery Lab when you can confidently explain:

1. Tracked vs untracked files.
2. Working Tree vs Staging Area vs Repository.
3. Branch pointers and HEAD.
4. Detached HEAD behavior.
5. Merge vs Rebase.
6. Reset vs Restore.
7. Reset vs Revert.
8. Soft, Mixed, and Hard resets.
9. Reflog recovery workflows.
10. Interactive rebase operations.
11. Merge commit parent relationships.
12. Force push implications.
13. Stash workflows.
14. Remote vs Local repositories.
15. Commit graph evolution after every operation.

---

# Final Goal
## note the solutions is at the local repo of the dev. and scattered across the commits of this project to get them ask for it
