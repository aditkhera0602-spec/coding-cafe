1. Meaning of --global git config and omitting it
The global flag sets your name and email for every Git project on your computer. If you leave it out, those details only apply to the specific repository you are currently working in.

2. Contents of .git revealed by ls -a
Running ls -a shows hidden files, which is why .git shows up here but not in regular ls. Inside .git are all the backend files, settings, and commit history that Git uses to track the project.

3. Approximate untracked file count and identifying untracked code
Git was trying to track thousands of files inside .venv/. That folder contains virtual environment dependencies and code libraries that I did not write myself.

4. Difference in git status after creating .gitignore
Once .gitignore was added, all the files inside .venv/ disappeared from the untracked list in git status. Only .gitignore itself showed up as an untracked file.

5. Why .gitignore itself should be committed rather than ignored
.gitignore needs to be committed so that the rules for ignoring files stay with the repo. That way, anyone else working on the project will not accidentally commit unnecessary files like .venv/ either.

6. Movement of README.md across sections in git status
It moved from Untracked files to Changes to be committed. In the three-places model, running git add moved the file from the working directory into the staging area.

7. Output produced by git commit and count of changed files
Git printed a summary with a short commit hash and the commit message. It showed that 1 file was changed, since that was the total number of files I had staged.

8. Name and purpose of the first seven characters of a commit hash
They are called the short commit hash. They act as a unique ID for the commit, so you can easily refer to that specific commit later.


