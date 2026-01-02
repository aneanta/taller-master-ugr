# Exercise Outcomes Submission Template

**Student/Group Name**: Ane Anta (Group X)  
**Level Completed**: master-of-the-universe  
**Date**: 2026-01-02

---

## 📋 Exercise Summary

### Exercise: Master of the Universe Level – Security and Governance (Branch Protection, Signed Commits, Auditing)
**Status**: ✅ Completed

**What I did**:
I configured secure repository governance on my fork by enabling branch protection rules for `main` so that changes must be made via Pull Request (direct pushes are blocked). I generated/configured a GPG key and produced verified (signed) commits. I also prepared security documentation artifacts (public key export and protection rules summary) and collected command outputs as evidence for evaluation.

**Commands Used**:
```bash
git checkout
git pull
git add
git commit
git push
git branch -a
git log --oneline --graph --all --decorate
git log --show-signature
gpg --full-generate-key
gpg --list-secret-keys --keyid-format=long
gpg --armor --export

```

**Results/Output**:
```
# Paste relevant command outputs, git log, or status messages
# Example:
$ git status
On branch group-X-outcomes/master-of-the-universe
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   OUTCOME_TEMPLATE.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        OUTCOMES.md
        gpg-test.txt
        gpg-test.txt.asc
        security-artifacts/




$ git branch -a
  feature/awesome-feature
  feature/footer
  feature/header
  feature/my-info
  feature/protected-main-test
  feature/signed-commits
  group-X-outcomes/intermediate
  group-X-outcomes/master
* group-X-outcomes/master-of-the-universe
  group-X-outcomes/newbie
  intermediate
  main
  master
  master-of-the-universe
  newbie
  remotes/origin/HEAD -> origin/main
  remotes/origin/feature/my-info
  remotes/origin/feature/protected-main-test
  remotes/origin/feature/signed-commits
  remotes/origin/group-X-outcomes/intermediate
  remotes/origin/group-X-outcomes/master
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




$ git log --oneline --graph --all --decorate -30
* 9ea3298 (origin/feature/signed-commits, feature/signed-commits) feat: add second signed commit
* 0b517a8 feat: add first signed commit
* b06928a (origin/feature/protected-main-test, feature/protected-main-test) test: change via PR workflow
* 9602351 (upstream/main, origin/main, origin/HEAD, main) Adding GenAI guidelines
* 7ad3af4 docs: update main branch files to reflect consolidated exercise structure (1 per level)
* 4d9131e chore: remove instructor files from repository tracking
*   adbb307 Merge pull request #9 from miguel-oltra/patch-gitignore-update
|\  
| * e4709e6 Updated CODEOWNERS file
| * 2a39a02 chore: add INSTRUCTOR_GUIDE.md to gitignore
| * 0abdbae chore: add SUMMARY.md to gitignore for instructor files
|/  
* 88a54ab chore: Add .gitignore to exclude instructor files and sensitive data
* e39ff08 PROMPT for updated
* df1cfdd fix: Update CODEOWNERS to allow trainee work while protecting exercise branches
* a011fad config: Add CODEOWNERS file for code review requirements
* 769be64 docs: Add complete implementation summary
* 9d008fa Updated README.MD with guidelines for the exercises
* f66bf22 docs: Update MODEL_SPEC.MD with PROMPT 2 requirements
* c24fd57 docs: Add outcome submission process and evaluation criteria
* ec488d0 Update main README with complete training overview and navigation
| * 0a3b8e3 (origin/group-X-outcomes/master, group-X-outcomes/master) docs: Add master level exercise outcomes for Group X
| | * c84a796 (feature/awesome-feature) Add awesome feature
| |/  
| * 0a67c2a (master) Update on master branch
| * bccaafb Add feature B
| * 6b93cdb Add feature A
| * b031894 Add complete configuration file
| * b5d8eb6 (upstream/master, origin/master) refactor: consolidate master exercises into single comprehensive exercise on history rewriting
| * 960a0a6 docs: Add submission instructions to master level
| * f0055a0 Update README for master level exercises
|/  
| * 10720af (origin/group-X-outcomes/intermediate, group-X-outcomes/intermediate) docs: Add intermediate level exercise outcomes for Group X
| *   4236520 (tag: v1.0-test, tag: v1.0, origin/intermediate, intermediate) Merge footer with resolved conflicts
| |\  




$ git log --show-signature -2
commit b0fb9dc0dfbe8a0cdf9099e70d6ea883e8fc8d14 (HEAD -> group-X-outcomes/master-of-the-universe, upstream/master-of-the-universe, origin/master-of-the-universe, master-of-the-universe)
gpg: Signature made Mon Dec 22 09:51:03 2025 CET
gpg:                using RSA key 1706CDE4E490D08BBEAD9756063BFCF906BA72B7
gpg: Can't check signature: No public key
Author: Miguel Angel Oltra <miguel.oltra@se.com>
Date:   Mon Dec 22 09:51:02 2025 +0100

    refactor: consolidate master-of-the-universe exercises into single comprehensive exercise

commit d1ef79fc28da80e9a124d2f48449c402f09d2ade
Author: Miguel Angel Oltra <SESA219665@se.com>
Date:   Sat Nov 29 12:11:47 2025 +0100

    docs: Add submission instructions to master-of-the-universe level




Additional evidence (branch protection enforced on main, direct push blocked):
remote: error: GH013: Repository rule violations found for refs/heads/main.
remote:
remote: - Changes must be made through a pull request.
To https://github.com/aneanta/taller-master-ugr.git
 ! [remote rejected] main -> main (push declined due to repository rule violations)
error: failed to push some refs to 'https://github.com/aneanta/taller-master-ugr.git'

```

---

## 🎯 Key Learnings

**Main concepts I learned**:
1. Branch protection rules (rulesets) can enforce secure workflows by requiring Pull Requests and blocking direct pushes.
2. GPG signing provides cryptographic verification of commits and supports “Verified” commits on GitHub once the public key is uploaded.
3. Security auditing and documentation (artifacts) are part of good governance: keys, rules, and evidence should be traceable and reproducible.

**Skills I improved**:
- Configuring branch protection rules for secure workflows.
- Generating and using GPG keys for signed commits.
- Collecting evidence and artifacts to support security auditing.

---

## 🚧 Challenges Faced

### Challenge 1: Direct push blocked by repository rules (GH013)
**Problem**: Direct pushes to main were rejected by GitHub repository rules

**Solution**: This confirmed branch protection was correctly enforced; changes must be made via Pull Request.


**Commands/Approach**:
```bash
git checkout main
git pull origin main
git commit -m "test: direct push to main"
git push origin main
```

---

### Challenge 2: GPG signing failed initially (terminal environment)
**Problem**: Signing failed with Inappropriate ioctl for device when trying to run git commit -S.

**Solution**: After configuring the environment/GPG agent appropriately, commits could be signed successfully and shown as “Good signature” locally.

**Commands/Approach**:
```bash
git commit -S -m "feat: add first signed commit"
git commit -S -m "feat: add second signed commit"
git log --show-signature -2

```
---

## 💭 Personal Reflection

**What surprised me**:
How strict branch protection can be and how clearly GitHub reports rule violations when a push is rejected.

**What I found most difficult**:
Getting GPG signing to work correctly in my terminal environment and understanding why signing can fail depending on the session configuration.

**What I found most useful**:
Learning the secure workflow: feature branch + Pull Request + signed commits. This is very close to real professional DevSecOps processes.

**How I would apply this in real projects**:
I would protect main (or master) with PR requirements and signing rules, use signed commits for accountability, and keep security artifacts/documentation as part of the repo to support audits and compliance.
---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic               | Confidence (1-5) | Notes                                     |
| ------------------- | ---------------- | ----------------------------------------- |
| Basic Git commands  | 4                | Comfortable with daily workflow           |
| Branching & merging | 4                | Confident with branches and merges        |
| Remote operations   | 4                | Fork workflow and remotes understood      |
| Conflict resolution | 3                | Comfortable with basic conflicts          |
| History rewriting   | 3                | Practiced in previous level               |
| Git hooks           | 1                | Not covered in this level                 |
| Security practices  | 4                | Branch protection + GPG signing practiced |

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/aneanta/taller-master-ugr/tree/group-X-outcomes/master-of-the-universe`
- Key commits demonstrating your work:
  - 9ea3298: feat: add second signed commit
  - 0b517a8: feat: add first signed commit
  - b06928a: test: change via PR workflow

**Additional files created** (if any):
- security-artifacts/public-key.asc: exported public GPG key (for verification)
- security-artifacts/protection-rules.txt: summary of applied branch protection rules and evidence
- signed-1.txt, signed-2.txt: files created for signed commit evidence

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
