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

9. The 4 steps of the repetitive Git loop
The loop consists of making changes to a file, running git status, staging the changes with git add, and saving them with git commit.

10. Special purpose and placement of README.md
README.md goes in the main folder so anyone opening the project gets an immediate summary of what it is. It gets a special name because GitHub automatically displays its contents on the repository's main page.

11. How gh auth login eliminates future password prompts
It links your terminal to your GitHub account using a secure token through the browser. Once that token is saved locally, GitHub CLI can use it to authenticate you when you interact with GitHub.

12. File rendered on GitHub's front page and the reason why
README.md is rendered on the front page. GitHub automatically converts the Markdown in this file into formatted text so it can be displayed as the project's description.

13. Effect of git push on local history
Running git push did not change anything on my local machine. It just copied the existing local commits to GitHub so the remote repository has those commits too.

14. Distinction between a private repository vs. no repository on GitHub
A private repository exists online, but only you and people you invite can see or access it. Having no repository means there is no online version or GitHub backup of the project.