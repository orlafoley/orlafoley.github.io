---
layout: page
title: Git Guide
permalink: /git-guide/
---

This guide will help you set up your GitHub to work on the Blog site.
The images are from an alternative repository but apart from the names everything should be the same.


---
## Setup

1. First, go to [The project repository](https://github.com/rh-outreach-blog/rh-outreach-blog.github.io).
  
2. Look for the **"fork"** button in the top right section of the view. See the below image:
![fork button](/images/fork-button.png)

3. Click this button then select an owner for your fork (your GitHub username should appear here) then click **"create fork"**.

4. Once you've created your fork, GitHub should take you directly to it. This should be identical to the project repo for now.

5. Click the green **"code"** button and copy the HTTPS address.

6. Within your terminal, navigate to whichever directory you store repositories in and enter:
    {% highlight bash %}
    git clone <THE_URL_YOU_COPIED>
    {% endhighlight %}

7. Once this has completed, navigate to the newly created directory by entering:
    {% highlight bash %}
    cd <NAME_OF_YOUR_DIR>
    {% endhighlight %}

8. Once you're in your repo's directory, let's check that our remote origin is set up correctly. Enter the following:
    {% highlight bash %}
    git remote show origin
    {% endhighlight %}

9. The **"Fetch-URL"** and **"Push URL"** should be in the format:
    {% highlight bash %}
    Fetch URL: https://github.com/<YOUR_USERNAME>/rh-outreach-blog.github.io.git
    Push  URL: https://github.com/<YOUR_USERNAME>/rh-outreach-blog.github.io.git
    {% endhighlight %}

10. If they aren't in this format you can update them using the following command:
    {% highlight bash %}
    git remote set-url <YOUR_REPO_URL>
    {% endhighlight %}

11. In the IDE of your choice, open this project directory. If using VS code you can do this by navigating to the directory and entering:
    {% highlight bash %}
    code .
    {% endhighlight %}

---
## Making Changes

1. A good practice when working on your code is to sync your fork regularly. Clicking the button will tell you if your fork is after falling behind the main repo. If so, click **"update branch"** to bring it up to date with the main repo. See below image:
![update fork](/images/update-fork.png)

2. Once you've synced your fork, you can pull any changes by using the command:
    {% highlight bash %}
    git pull
    # or if that doesn't work
    git pull origin main
    {% endhighlight %}

3. Now let's add a new blog page. To do this, navigate to **docs/_posts** within the project repo.

4. Let's create a branch for the changes we intend to make to the upsteam repo. Do this by entering:
    {% highlight bash %}
    git checkout -b <YOUR_BRANCH_NAME> # -b flag will create the branch prior to checkout
    {% endhighlight %}

5. Within this directory, create a new file with the name format: **YYYY-MM-D-<ENTRY_TITLE>.markdown**. Note that it must be a current or past date.

6. Next open the sample file **2024-11-4-sample_blog.markdown**, copy its contents and paste them into your new file.

7. Update the section at the start of the file as seen below:
    {% highlight bash %}
    ---
    layout: post # leave as is
    title:  "<NEW_BLOG_TITLE>" # add whatever title you'd like
    date:   <YYYY-MM-D> <HH:MM:SS> +0100 # update the date and time
    categories: jekyll update # leave as is
    ---
    {% endhighlight %}

8. Make whatever changes you like to the repo and save them within your IDE.

9. Now lets add these changes to stage. In your integrated terminal enter:
    {% highlight bash %}
    git add .
    {% endhighlight %}

10. Now that we've staged the changes, we can commit them:
    {% highlight bash %}
    git commit -m "<YOUR_COMMIT_MESSAGE>"
    {% endhighlight %}

11. You can check if your commit was successful by entering:
    {% highlight bash %}
    git log
    {% endhighlight %}

12. Once you've verified the presence of your commit, you can push it to your origin by entering:
    {% highlight bash %}
    git push origin <YOUR_BRANCH_NAME> # this will create a remote branch of the same name and push it
    {% endhighlight %}


---
## Opening a PR(Pull Request)

1. The changes you've made should now be present in your remote branch. Check this by navigating to your repository on GitHub and click the branch button seen in the below screenshot.
![branch button](/images/branch-icon.png)

2. Verify that your remote branch contains the most recent commit.
   
3. In order to submit a PR we need to ensure our upsteam origin is set. Enter the following:
    {% highlight bash %}
    git remote add upstream https://github.com/rh-outreach-blog/rh-outreach-blog.github.io.git
    {% endhighlight %}

4. Now you can enter the following to create a PR:
    {% highlight bash %}
    gh pr create --base main --head <YOUR_USERNAME>:<BRANCH_NAME> --repo rh-outreach-blog/rh-outreach-blog.github.io --title "Your PR Title" --body "Your PR Description"
    {% endhighlight %}




