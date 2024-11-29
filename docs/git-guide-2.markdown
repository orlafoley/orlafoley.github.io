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
    ```

2. Let's make a change to this branch. Add the text "This is a test" to the README file via your IDE or simplt enter:
    ``` bash 
    echo -e "\n    This is a test" >> README.md
    ```

3. Save your change then enter:
    ``` bash
    git add . # this will add all of the changed files within the current directory to staging
    ```

4. Next we'll commit this change by entering:
    ``` bash
    git commit -m "This is the first change"
    ```

5. Verify the presence of this commit by entering:
    ``` bash
    git log
    ```

6. Let's make a second change:
    ``` bash
    echo -e "\n    This is the second test" >> README.md
    ```

7. Hit save but do **NOT** add this change to staging.

8. Now we will attempt to move back to our main branch:
    ``` bash
    git checkout main
    ```
    This should result in an error:
    ``` bash
        error: Your local changes to the following files would be overwritten by checkout:
            README.md
    Please commit your changes or stash them before you switch branches.
    Aborting
    ```
9. Let's stash the uncommited changes before switching to main:
    ``` bash
    git stash
    ```
    Then:
    ``` bash
    git checkout main
    ```
10. You should obverve that the changes made in your branch are not reflected in main. Let's switch back to our test branch:
    ``` bash
    git checkout exercise-2
    ```

11. Now we can continue on our stashed changes by entering:
    ``` bash
    git stash apply
    ```

12. Let's commit the changes:
    ``` bash
    git commit -m "This is the second change"
    ```

---
## Rebasing

1. Let's examine our current git log:
    ``` bash
    git log
    ```




