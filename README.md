# Liftoff-GitWorkflowDemo
A demonstration of using a git repository cooperatively with another developer

## PART 1 - SETUP

#### A. Fork this repo!

1. Just ONE team member should fork this repo to their own account.

#### B. Make sure everyone is a collaborator on the repo.
<img width="1200" alt="Screen Shot 2022-04-17 at 7 36 23 PM" src="https://user-images.githubusercontent.com/55961845/163738252-22b04898-c6b3-46e8-bae1-aff1e22f6229.png">

1. Go to Settings > Collaborators.
2. Use the e-mail address associated with each other teammate's GitHub accounts to invite them.
3. They will each have to accept the request from the e-mail they receive.

#### C. Each person needs a copy on their local machine.

1. DO NOT FORK THE REPO. Then you will no longer actually still be working on the same project.
2. As collaborators, you should all have permissions to contribute code, merge each other's code, etc.
3. Clone the repo as-is. Grab the URL, open a terminal, and use `git clone <repo-url>` to place it where you want on your local machine.
4. Open your cloned `Liftoff-GitWorkflowDemo` folder in the IDE of your choice (probably VSCode or IntelliJ).
5. Keep a terminal open, whether it's in the IDE or otherwise.

---

## PART 2 - ONE BRANCH, MULTIPLE CONTRIBUTORS

#### A. Create a new branch and commit a change.

1. Have ONE teammate create a new branch on their local machine using `git checkout -b practice-feature-branch`.
2. Create a new markdown file next to this README, called `team.md`.
3. Add your name to the file, then save.
4. In your terminal, use `git status` to verify the new file is untracked and unstaged.
5. Then use `git add .` to stage the file.
6. Use `git status` again to verify the file has been staged.
7. Use `git commit -m "Added the name <yourname> to team.md"` to make the commit.

#### B. Push the new branch to GitHub.

1. Since this new, locally-created branch has never been pushed to the remote repo, you need to set the upstream path while you're at it. Use `git push -u origin practice-feature-branch` to do this now. 
2. Good! Now the branch with the commit you made should be available to everyone else.
> Note: any further changes you or anyone else makes to this branch now will require only `git push`.

#### C. Each team member should contribute (one at a time).

1. From your local machine, in the `main` branch, use `git pull` to update your local repo. You'll see that it now has knowledge of the branch your teammate created.
> Try this: enter `git branch`. Do you see the new branch? No? That's because you don't have a local copy yet. Try `git branch -r` to list only remote branches. There it is!
3. Create and switch to a local copy of this new remote branch using `git checkout practice-feature-branch`.
4. Open `team.md` in your IDE. You should see the names of anyone who already contributed. Now add your name and save the file.
5. Go through the verify/add/verify process with `git status`, `git add .`, and `git status`.
6. Now use `git commit -m "Added the name <yourname> to team.md"` to make the commit and `git push` to send it up to GitHub.
7. Each remaining team member should repeat steps 1-6. 

---

## PART 3 - PULL REQUEST & MERGE TO MAIN

#### A. View changes on GitHub.

1. Each person should take a look at the repository on GitHub in their browser. 
2. You can view the new branch, view the list of commits, and more. 
3. Go back and forth between `main` and `practice-feature-branch` to see that one version has the new file and the other does not. Let's change that!

#### B. Open a pull request and review changes.

1. ONE team member should open a pull request for the new branch.
2. Once it's open, everyone can go to the PR page. 
3. Click on the "Files changed" tab to see the diff.
4. From here, one or more other team members can review and comment on the changes. Try it!

<img width="974" alt="Screen Shot 2022-04-17 at 8 27 22 PM" src="https://user-images.githubusercontent.com/55961845/163740602-a75b2b4a-389e-4742-9da3-fca7746729f2.png">

#### C. Approve the PR and merge the branch into main.

1. Someone *other* than the person who opened the PR should approve and merge the branch.
2. Once it's done, you can choose to delete the remote copy of the feature branch. Up to you.
3. If everyone now goes to the main branch and views the files, you should see BOTH markdown files are now a part of `main`.

#### Great job!
