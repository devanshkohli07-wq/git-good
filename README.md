# Git Bisect Practice (No Code Required)

This branch is designed to practice `git bisect` using a text file.

Steps:
1. Checkout this branch: `git checkout bisect-practice`
2. Start bisect: `git bisect start`
3. Mark the latest commit as bad: `git bisect bad`
   - Because `notes.txt` contains "BUG introduced here".
4. Mark the first commit as good: `git bisect good <commit-hash>`
   - The initial commit only says "Everything is fine."
5. Git will check out commits between good and bad.
6. Open `notes.txt` at each step:
   - If it contains "BUG introduced here", run `git bisect bad`
   - Otherwise, run `git bisect good`
7. Continue until Git identifies the exact commit that introduced the bug.
8. Reset bisect: `git bisect reset`
