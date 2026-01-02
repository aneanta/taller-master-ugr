# Exercise Outcomes Submission Template

**Student/Group Name**: Ane Anta (Group X)  
**Level Completed**: newbie  
**Date**: 2026-01-02

---

## 📋 Exercise Summary

### Exercise: Newbie Level – Git Basics
**Status**: ✅ Completed

**What I did**:  
I completed the newbie-level Git exercise by working with the basic Git workflow. I created and tracked files, staged and committed changes, explored the commit history, created and switched branches, and worked with remote repositories. I also created a feature branch, pushed it to my forked repository, and documented the exercise results in an outcome branch.

**Commands Used**:
```bash
git clone
git checkout
git status
git add
git commit
git log
git branch -a
git checkout -b
git push
git pull
git remote -v
git fetch


**Results/Output**:
```
# Paste relevant command outputs, git log, or status messages
# Example:
$ git log --oneline -5
7c4eb22 (HEAD -> group-X-outcomes/newbie, newbie) Add personal information
61876cd (origin/newbie) Adding hello.txt with my name
360f4a4 (upstream/newbie) refactor: consolidate newbie exercises into single comprehensive exercise
5eedc97 docs: Add submission instructions to newbie level
45e1c31 Update README for newbie level exercises

$ git branch -a
  feature/my-info
* group-X-outcomes/newbie
  main
  newbie
  remotes/origin/HEAD -> origin/main
  remotes/origin/feature/my-info
  remotes/origin/intermediate
  remotes/origin/main
  remotes/origin/master
  remotes/origin/master-of-the-universe
  remotes/origin/newbie
  remotes/upstream/intermediate
  remotes/upstream/main
  remotes/upstream/master
  remotes/upstream/master-of-the-universe
  remotes/upstream/newbie

## 🎯 Key Learnings

**Main concepts I learned**:
1. How Git manages files using the working directory, staging area, and commits.
2. How to create and switch branches.
3. How local branches track remote branches.

**Skills I improved**:
- Using git status and git log to inspect repository state.
- Managing feature branches.
- Working with multiple remotes (origin and upstream).

---

## 🚧 Challenges Faced

### Challenge 1: Permission denied when pushing
**Problem**: I received a 403 error when trying to push directly to the instructor repository.

**Solution**: I created a fork of the repository and updated the origin remote to point to my fork.

**Commands/Approach**:
git remote set-url origin https://github.com/aneanta/taller-master-ugr.git
git push origin feature/my-info


---

### Challenge 2: Remote branch not found
**Problem**: Running git pull origin newbie failed because the newbie branch did not exist in my fork.

**Solution**: I added the instructor repository as upstream and configured my local newbie branch to track upstream/newbie.

**Commands/approach**:
git remote add upstream https://github.com/miguel-oltra/taller-master-ugr.git
git fetch upstream
git branch --set-upstream-to=upstream/newbie newbie
git pull

---

## 💭 Personal Reflection

**What surprised me**:
How important understanding remotes is when working with forks.

**What I found most difficult**:
Understanding branch tracking and remote references.

**What I found most useful**:
Learning the standard fork-based workflow used in collaborative projects.

**How I would apply this in real projects**:
I would use feature branches and pull requests to collaborate safely.

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic               | Confidence (1-5) | Notes                                      |
| ------------------- | ---------------- | ------------------------------------------ |
| Basic Git commands  | 4                | Comfortable with status, add, commit, log  |
| Branching & merging | 3                | Confident with basic branching             |
| Remote operations   | 3                | Understand origin vs upstream after issues |
| Conflict resolution | 1                | Not covered in this level                  |
| History rewriting   | 1                | Not covered in this level                  |
| Git hooks           | 1                | Not covered in this level                  |
| Security practices  | 1                | Not covered in this level                  |


---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/aneanta/taller-master-ugr/tree/group-X-outcomes/newbie`
- Key commits demonstrating your work:
  - 61876cd — Adding hello.txt with my name
  - daa1cc0 — Adding personal information

**Additional files created** (if any):
- hello.txt: File containing my name.
- my-info.txt: File containing personal information and motivation.

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [x] Completed the exercise for your chosen level (including all parts)
- [x] Documented all commands used with their outputs
- [x] Described challenges and how you resolved them
- [x] Provided a thoughtful reflection on your learning
- [x] Self-assessed your confidence in each topic
- [x] Pushed your outcome branch to the remote repository
- [] Created a Pull Request (if required by your instructor)


**Submission Date**: [02/01/2026]  
**Ready for Review**: ✅ Yes
