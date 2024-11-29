---
layout: page
title: Exercise 2
permalink: /git-guide-2/
---

This guide will allow you to put the learning from lessons 4 - 6 into practice. It will walk you through the process of:

* Opening a new branch and making changes there
* Stashing these changes to safely switch branches
* Rebasing your branch to tidy your commit history

This exercise operates on the expectation that you have completed exercise 1, if not, please do so and return to this guide.

---
## Stashing changes

1. Within your IDE, open the project directory and enter the following in your integrated terminal:
    ``` bash
    git checkout -b exercise-2 # this will create and switch to a new branch for this exercise

2. Let's make a change to this branch. Add the text "This is a test" to the README file via your IDE or simplt enter:
    ``` bash 
    echo -e "\n    This is a test" >> README.md

3. Save your change then enter:
    ``` bash
    git add . # this will add all of the changed files within the current directory to staging

4. testing



---
## Opening a PR(Pull Request)

1. The changes you've made should now be present in your remote branch. Check this by navigating to your repository on GitHub and click the branch button seen in the below screenshot.
![branch button](/images/branch-icon.png)

2. Verify that your remote branch contains the most recent commit.
   
3. In order to submit a PR we need to ensure our upsteam origin is set. Enter the following:
    ``` bash
    git remote add upstream https://github.com/rh-outreach-blog/rh-outreach-blog.github.io.git
    ```

4. Now you can enter the following to create a PR:
    ``` bash
    gh pr create --base main --head <YOUR_USERNAME>:<BRANCH_NAME> --repo rh-outreach-blog/rh-outreach-blog.github.io --title "Your PR Title" --body "Your PR Description"
    ```




