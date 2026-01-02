# Exercise Outcomes Submission Template

**Student/Group Name**: Ane Anta (Group X)  
**Level Completed**: master  
**Date**: 2026-01-02

---

## 📋 Exercise Summary

### Exercise: Master Level – History Rewriting (amend, rebase, interactive rebase)
**Status**: Completed

**What I did**:  
In this exercise, I practiced advanced Git techniques focused on rewriting history. I created a commit and then updated it using `git commit --amend`. I created multiple commits and then used interactive rebase (`git rebase -i`) to clean up the history by squashing/fixing up a commit. Finally, I created a feature branch and rebased it on top of the updated master branch to maintain a linear history.

**Commands Used**:
```bash
git checkout
git checkout -b
git status
git add
git commit
git commit --amend
git rebase
git rebase -i
git log
git log --oneline --graph --all --decorate

```

**Results/Output**:
```
# Paste relevant command outputs, git log, or status messages
# Example:
$ git status
On branch group-X-outcomes/master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   OUTCOME_TEMPLATE.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        OUTCOMES.md



$ git log --oneline --graph --all --decorate -20
* c84a796 (HEAD -> feature/awesome-feature) Add awesome feature
* 0a67c2a (master) Update on master branch
* bccaafb Add feature B
* 6b93cdb Add feature A
* b031894 Add complete configuration file
* b5d8eb6 (upstream/master, origin/master) refactor: consolidate master exercises into single comprehensive exercise on history rewriting
* 960a0a6 docs: Add submission instructions to master level
* f0055a0 Update README for master level exercises
| * 10720af (origin/group-X-outcomes/intermediate, group-X-outcomes/intermediate) docs: Add intermediate level exercise outcomes for Group X
| *   4236520 (tag: v1.0-test, tag: v1.0, origin/intermediate, intermediate) Merge footer with resolved conflicts
| |\  
| | * ff84dc7 (feature/footer) Add footer to page
| * | 1dc3f8a (feature/header) Add header to page
| |/  
| * 994450b (upstream/intermediate) refactor: consolidate intermediate exercises into single comprehensive exercise
| * a1c17e7 docs: Add submission instructions to intermediate level
| * 9f25f7a Update README for intermediate level exercises
|/  
| * 73dd8d9 (origin/group-X-outcomes/newbie, group-X-outcomes/newbie) docs: Add newbie level exercise outcomes for Group X
| * 7c4eb22 (newbie) Add personal information
| | * daa1cc0 (origin/feature/my-info, feature/my-info) Adding personal information
| |/  
| * 61876cd (origin/newbie) Adding hello.txt with my name
| * 360f4a4 (upstream/newbie) refactor: consolidate newbie exercises into single comprehensive exercise


## 🎯 Key Learnings

**Main concepts I learned**:
1. git commit --amend rewrites the last commit by replacing it with a new commit (new hash).
2. git rebase -i can be used to clean up commit history to make it more readable.
3. Rebasing a feature branch onto master allows keeping a linear history without merge commits.

**Skills I improved**:
- Cleaning and structuring Git history for professional workflows.
- Understanding how and why commit hashes change after history rewriting.
- Using rebase to align feature branches with the latest master changes.

---

## 🚧 Challenges Faced

### Challenge 1: Understanding history rewriting consequences
**Problem**: After using git commit --amend and git rebase -i, the commit hashes changed. This can be confusing at first and can cause issues if the rewritten history had already been pushed/shared.

**Solution**: I learned that rewriting history should be done only on private/local branches (or branches not used by others). It is safe before pushing or when working alone, and it keeps history clean and readable. 

**Commands/Approach**:
```bash
git commit --amend -m "Add complete configuration file"
git rebase -i HEAD~3

```

---

### Challenge 2: Rebasing a feature branch on master
**Problem**: Ensuring the feature branch commit stayed on top of the latest master commit without creating a merge commit.

**Solution**: I rebased the feature branch onto master, resulting in a linear history with the feature commit applied after the master update.

---

## 💭 Personal Reflection

**What surprised me**:
I would use --amend for quick fixes to the last commit before pushing, and interactive rebase to clean up my feature branch before opening a pull request. I would avoid rewriting history on shared branches.

**What I found most difficult**:
Learning how to maintain a clean, linear history using rebase, which is often preferred in professional repositories.

**What I found most useful**:
Understanding the implications of rewriting history and when it is appropriate to use these commands.

**How I would apply this in real projects**:
I would use --amend for quick fixes to the last commit before pushing, and interactive rebase to clean up my feature branch before opening a pull request. I would avoid rewriting history on shared branches.

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic               | Confidence (1-5) | Notes                                          |
| ------------------- | ---------------- | ---------------------------------------------- |
| Basic Git commands  | 4                | Comfortable with standard workflow             |
| Branching & merging | 4                | Confident creating and managing branches       |
| Remote operations   | 3                | Confident with fork workflow (origin/upstream) |
| Conflict resolution | 3                | Comfortable resolving basic conflicts          |
| History rewriting   | 4                | Comfortable with amend and rebase              |
| Git hooks           | 1                | Not covered in this level                      |
| Security practices  | 1                | Not covered in this level                      |


---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/aneanta/taller-master-ugr/tree/group-X-outcomes/master`
- Key commits demonstrating your work:
  - b031894 — Add complete configuration file (amend result)
  - bccaafb — Add feature B (after interactive rebase)
  - 6b93cdb — Add feature A
  - 0a67c2a — Update on master branch
  - c84a796 — Add awesome feature (feature branch)

**Additional files created** (if any):
- awesome.txt
- master-update.txt
- featureB.txt
- featureA.txt
- config.txt

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [x] Completed the exercise for your chosen level (including all parts)
- [x] Documented all commands used with their outputs
- [x] Described challenges and how you resolved them
- [x] Provided a thoughtful reflection on your learning
- [x] Self-assessed your confidence in each topic
- [ ] Pushed your outcome branch to the remote repository
- [ ] Created a Pull Request (if required by your instructor)

---

**Submission Date**: [2026-01-02]  
**Ready for Review**: ✅ Yes 
