# Instructions

In this assignment, you will familiarize yourself with three common **version control** workflows using **`git`** and **GitHub**: (1) a **centralized workflow**, (2) a branch-based (a.k.a. feature based) workflow, and (3) a **forking workflow** (also known as the **"open source workflow"**).

With the centralized workflow, you will set up a **remote** repository on GitHub and a **local** **cloned** **repository** for your own project and practice **pushing** and **pulling** to/from this remote repository on the main branch.

With the branch-based workflow, you will still use the same repository above but you will not directly work on the main branch. Instead, you will create a branch with your updates and then merge this branch using a **pull request**.

With the forking workflow, you will contribute to another student's project by **forking** their repository, making changes to your copy, and issuing a **pull request** to them to incorporate your changes.

Note that with version control systems such as `git`, it is easy to verify what work has or has not been done by whom on any project via the git log. 

Execute the following instructions in order.


## Part 1: Centralized workflow

In this part, we will try out a simple **centralized workflow**, where developers work with two copies of a repository: a **local** copy, where changes are made; and a **remote** copy, where completed changes are uploaded in order to be archived and shared with others.


### Create a local Git repository

1.  Clone your remote repository on GitHub to your own local machine.

2. Make sure to change directories to the new directory that got created with your cloned repo.

3.  Create a file called `ARTICLE.md` and edit it to include the following:
    - a link to an article or web site you find interesting related to software development/engineering 
    - a short paragraph or two about what you find interesting about that article
    - remember that this will be public
    - Use Markdown syntax to make it look nice
    
3.  **Commit** your `ARTICLE.md` file to the local repository, including a meaningful commit message.

4. Edit the `README.md` file in the repo to include your name. Commit your change using a meaningful commit message.

### Push changes to the upstream remote repository

1.  **Commit** and **Push** the latest version of these two files in your local repository to your Github repository.
2.  Your two repositories should now be in-sync (i.e., what you see on your local machine should look the same as what you see on your repository on github.com)

## Part 2: Use branches for a branch-based/feature-based workflow

Note that this is the workflow you will be using for your group projects. However, in the group project, you will be working with other team members who will review your Pull Requests. Since this is an individual repo, we will ignore code review in this step but you will practice it in Part 3 below.

### Create a branch

1. Create a new branch in your repo using `git checkout -b <yourname>/proofread` . For example, if I were creating this branch for myself I would use `git checkout -b snadi/proofread` or `git checkout -b sarah/proofread`

### Make changes on this branch

1. Carefully proof read the content in `ARTICLE.md` and fix any typos. Add a new section at the bottom of the document called `Proof Reading` and type the sentence "Article checked for typos"
2. Commit your changes and push them. Note that these changes are pushed to the new branch. Since this is your first time pushing to the branch, git will ask you to first set the upstream for this branch. Simply run the command it asks you to and then push.

### Create a Pull Request

1. Go to your repository on github and go to Pull Requests
2. Create a new pull request to merge the changes from your branch into the `main` branch (see [Make a pull request](https://help.github.com/articles/creating-a-pull-request/))

### Merge the Pull Request

1. Merge the pull request using the merge button on github
2. Go to your local repo and switch to the main branch (`git checkout main`)
3. Pull the latest changes using `git pull` (remember that the changes from the branch have been merged into main on the remote repository on github but your local repo still doesn't know about it and that's why this step is necessary)
4. If you view the contents of `ARTICLE.md` on your local machine, you should see the new section and statement above.

### Share your repository with others

1.  Share the link to your GitHub repository as a new thread on the [course forum](https://brightspace.nyu.edu/d2l/le/434760/discussions/topics/515291/View) and invite others to collaborate... they will do so via the **forking workflow** outlined below. 

## Part 3: Forking workflow

In this part, we will practice the **forking workflow**, also known as the **open source workflow**. Developers following this type of workflow interact with at least 3 different copies of a repository: the original **remote** repository that the developer ultimately intends to contribute to; a remote **clone** of that official repositor, known as a "`fork`"; and a local clone of the fork, where the developer makes changes.

### Find another repository to work with

1.  Wait for other students to also share their repository links from the centralized workflow part of this assignment.
2.  Select one of the other students' GitHub repository links that you find interesting.

### Fork that repository

1.  **Fork** that repository on GitHub - you now have a clone of that repository in your own GitHub account - we'll refer to this repository as "your forked repository"

### Make a local clone of that fork

1.  **Clone** your forked repository from GitHub to a new directory on your local machine (not the same directory as your original repository). You are now working on the main branch of the forked repo.

### Make some edits

1.  Edit the `ARTICLE.md` file in your forked repository on your local machine to include a comment from you about that same article mentioned in the file. Make it look nice using Markdown syntax.
    - Include your name in the edit you make, so we can clearly see who did it (we can also verify this with the Git change logs)
2.  Commit these changes to your local repository, including a meaningful commit message

### Push changes to your remote fork

1.  **Pull** any changes others may have made to the remote repository on GitHub while you were working (use the `--rebase` option on the git pull to put your own changes to the tip of the change history when merged. i.e., `git pull --rebase`)
2.  **Push** your changes to your remote fork repository on GitHub

### Issue a pull request to the original repository

1.  [Make a pull request](https://help.github.com/articles/creating-a-pull-request/) on the other student's original repository from which you forked yours, asking them politely to include your changes in their original repository
2. Make sure that your PR eventually gets merged before the assignment due date. 
3. Update the README file of your original repository from the centralized workflow to include the link to your merged PR. 

### Accept contributions to your repository

1.  Make sure at least one other student has made a pull request with some changes to your own original repository - use the forum to coordinate this
2.  If the pull request has changes you dislike, leave a code review indicating why you have not accepted them, asking the other contributor to fix the problems. Leave at least one code review, even if it is just a positive comment (we want you to practice creating code review comments)
3.  Once you are happy with the changes, accept them and merge the pull request into your main branch
4.  Pull the updated files to the local repository of your project

