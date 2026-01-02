# Exercise Outcomes Submission Template

**Student/Group Name**: Ane Anta (Group X)  
**Level Completed**: intermediate  
**Date**: 2026-01-02

---

## 📋 Exercise Summary

### Exercise: Intermediate Level – Merging, Conflicts and Tags
**Status**: Completed

**What I did**:  
In this exercise, I worked with multiple branches to simulate a collaborative workflow. I created two feature branches (`feature/header` and `feature/footer`) that modified the same file, which caused a merge conflict. I resolved the conflict manually and completed the merge. After that, I created both annotated and lightweight tags to mark a release version. Finally, I documented the entire process in an outcome branch.

**Commands Used**:
```bash
git checkout
git checkout -b
git status
git add
git commit
git merge
git log
git log --oneline --graph --all --decorate
git tag
git show
git push
git branch -a
```

**Results/Output**:
```
# Paste relevant command outputs, git log, or status messages
# Example:
$ git status
On branch group-X-outcomes/intermediate
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   OUTCOME_TEMPLATE.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        OUTCOMES.md


$ git branch -a
  feature/footer
  feature/header
  feature/my-info
* group-X-outcomes/intermediate
  group-X-outcomes/newbie
  intermediate
  main
  newbie
  remotes/origin/HEAD -> origin/main
  remotes/origin/feature/my-info
  remotes/origin/group-X-outcomes/newbie
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



$ git log
commit 42365206a25809c84238bdf0842f8825589748f2 (HEAD -> group-X-outcomes/intermediate, tag: v1.0-test, tag: v1.0, origin/intermediate, intermediate)
Merge: 1dc3f8a ff84dc7
Author: aneanta <aneanta15@gmail.com>
Date:   Fri Jan 2 18:52:51 2026 +0100

    Merge footer with resolved conflicts

commit ff84dc786c59010f2e2bf8479c7ea89f473d0947 (feature/footer)
Author: aneanta <aneanta15@gmail.com>
Date:   Fri Jan 2 18:50:59 2026 +0100

    Add footer to page

commit 1dc3f8ae9d9d5ee06922262b26c19f185089b3c3 (feature/header)
Author: aneanta <aneanta15@gmail.com>
Date:   Fri Jan 2 18:50:49 2026 +0100

    Add header to page

commit 994450ba63e2b0cbe4a271a6efcb89c9cf850951 (upstream/intermediate)
Author: Miguel Angel Oltra <miguel.oltra@se.com>
Date:   Mon Dec 22 09:44:39 2025 +0100

    refactor: consolidate intermediate exercises into single comprehensive exercise



$ git log --oneline --graph --all --decorate
*   4236520 (HEAD -> group-X-outcomes/intermediate, tag: v1.0-test, tag: v1.0, origin/intermediate, intermediate) Merge footer with resolved conflicts
|\  
| * ff84dc7 (feature/footer) Add footer to page
* | 1dc3f8a (feature/header) Add header to page
|/  
* 994450b (upstream/intermediate) refactor: consolidate intermediate exercises into single comprehensive exercise
* a1c17e7 docs: Add submission instructions to intermediate level
* 9f25f7a Update README for intermediate level exercises
| * 73dd8d9 (origin/group-X-outcomes/newbie, group-X-outcomes/newbie) docs: Add newbie level exercise outcomes for Group X
| * 7c4eb22 (newbie) Add personal information
| | * daa1cc0 (origin/feature/my-info, feature/my-info) Adding personal information
| |/  
| * 61876cd (origin/newbie) Adding hello.txt with my name
| * 360f4a4 (upstream/newbie) refactor: consolidate newbie exercises into single comprehensive exercise
| * 5eedc97 docs: Add submission instructions to newbie level
| * 45e1c31 Update README for newbie level exercises
|/  
| * 9602351 (upstream/main, origin/main, origin/HEAD, main) Adding GenAI guidelines
| * 7ad3af4 docs: update main branch files to reflect consolidated exercise structure (1 per level)
| * 4d9131e chore: remove instructor files from repository tracking
| *   adbb307 Merge pull request #9 from miguel-oltra/patch-gitignore-update
| |\  
| | * e4709e6 Updated CODEOWNERS file
| | * 2a39a02 chore: add INSTRUCTOR_GUIDE.md to gitignore
| | * 0abdbae chore: add SUMMARY.md to gitignore for instructor files
| |/  
| * 88a54ab chore: Add .gitignore to exclude instructor files and sensitive data
| * e39ff08 PROMPT for updated
| * df1cfdd fix: Update CODEOWNERS to allow trainee work while protecting exercise branches
| * a011fad config: Add CODEOWNERS file for code review requirements
| * 769be64 docs: Add complete implementation summary
| * 9d008fa Updated README.MD with guidelines for the exercises
| * f66bf22 docs: Update MODEL_SPEC.MD with PROMPT 2 requirements
| * c24fd57 docs: Add outcome submission process and evaluation criteria
| * ec488d0 Update main README with complete training overview and navigation
|/  
| * b0fb9dc (upstream/master-of-the-universe, origin/master-of-the-universe) refactor: consolidate master-of-the-universe exercises into single comprehensive exercise
| * d1ef79f docs: Add submission instructions to master-of-the-universe level
| * 5bffa64 Update README for master-of-the-universe level exercises
|/  
| * b5d8eb6 (upstream/master, origin/master) refactor: consolidate master exercises into single comprehensive exercise on history rewriting
| * 960a0a6 docs: Add submission instructions to master level
| * f0055a0 Update README for master level exercises
|/  
* dc58203 Revert "Update README.md"
* e2db1ca (tag: v0.0.1) Update README.md
* 3d651c3 Update README.md
* 4cc5635 Initial commit


$ git tag
v0.0.1
v1.0
v1.0-test


$ git show v1.0
tag v1.0
Tagger: aneanta <aneanta15@gmail.com>
Date:   Fri Jan 2 18:53:28 2026 +0100

First stable version with merged features

commit 42365206a25809c84238bdf0842f8825589748f2
Merge: 1dc3f8a ff84dc7
Author: aneanta <aneanta15@gmail.com>
Date:   Fri Jan 2 18:52:51 2026 +0100

    Merge footer with resolved conflicts



$ git show v1.0-test
commit 42365206a25809c84238bdf0842f8825589748f2
Merge: 1dc3f8a ff84dc7
Author: aneanta <aneanta15@gmail.com>
Date:   Fri Jan 2 18:52:51 2026 +0100

    Merge footer with resolved conflicts

```

---

## 🎯 Key Learnings

**Main concepts I learned**:
1. How Git handles merge conflicts when multiple branches modify the same file.
2. How to manually resolve conflicts and complete a merge commit.
3. The difference between annotated tags and lightweight tags.

**Skills I improved**:
- Resolving merge conflicts.
- Reading and interpreting commit graphs.
- Using tags to mark release versions.

---

## 🚧 Challenges Faced

### Challenge 1: Merge conflict (add/add)
**Problem**: An add/add conflict occurred when merging feature branches that both added the same file.

**Solution**: I manually edited the file to include all required changes and completed the merge.

---

### Challenge 2: Understanding tags
**Problem**: Understanding the difference between annotated and lightweight tags.

**Solution**: I created both types and inspected them using git show.

---

## 💭 Personal Reflection

**What surprised me**:
How clearly Git visualizes merge history and conflict resolution.

**What I found most difficult**:
Understanding the internal representation of add/add conflicts.

**What I found most useful**:
Conflict resolution and tagging releases.

**How I would apply this in real projects**:
Using feature branches, careful merges, and tags for release management.

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic               | Confidence (1-5) | Notes                         |
| ------------------- | ---------------- | ----------------------------- |
| Basic Git commands  | 4                | Comfortable with fundamentals |
| Branching & merging | 4                | Confident resolving conflicts |
| Remote operations   | 3                | Confident with fork workflow  |
| Conflict resolution | 4                | Understood and applied        |
| History rewriting   | 1                | Not covered                   |
| Git hooks           | 1                | Not covered                   |
| Security practices  | 1                | Not covered                   |


---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/aneanta/taller-master-ugr/tree/group-X-outcomes/intermediate`
- Key commits demonstrating your work:
  - 4236520 — Merge footer with resolved conflicts
  - ff84dc7 — Add footer to page
  - 1dc3f8a — Add header to page

**Additional files created** (if any):
- page.html: Header and footer html

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [x] Completed the exercise for your chosen level (including all parts)
- [x] Documented all commands used with their outputs
- [x] Described challenges and how you resolved them
- [x] Provided a thoughtful reflection on your learning
- [x] Self-assessed your confidence in each topic
- [x] Pushed your outcome branch to the remote repository
- [ ] Created a Pull Request (if required by your instructor)


**Submission Date**: [2026-01-02]  
**Ready for Review**: ✅ Yes
