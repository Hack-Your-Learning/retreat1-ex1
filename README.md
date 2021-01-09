# Hack Your Learning: Session 1

## Introduction

The purpose of this exercise is to familiarize you with `git`. With your team you will follow the steps outlined on this page.

### What is .md?

Markdown is a syntax that allows you more functionality to format text. Popular social sites along with blogs will use markdown in various forms. Markdown is commonly used in `git` when creating documentation for your repository.

<https://www.ultraedit.com/company/blog/community/what-is-markdown-why-use-it.html>

### Perquisites

- A text editor
- A Github account
- `git` installed on your machine
- terminal or command prompt access

## Exercise 1: Git Basics

1. Make a copy of the repository on a member of your team's Github account. Do this by forking the repository. Navigate to the Hack Your Learning repository then click the fork button <https://github.com/Hack-Your-Learning/retreat1-ex1>
2. Each member of your team should clone this repository on their own computer. Do this by navigating to the folder of your choice within the command line and then using the command

```bash
git clone [your repository URL]
```

3. Once each member has cloned the repository, open the `lorem_ipsum.md` file located in the `storyTime` folder in your text editor of choice.
4. Get each team member to make a change to the file but don't indicate where the change has been made. Once you have made a change save the file. In your terminal commit the change by typing

```bash
git commit -a -m "your message here"
```

The core command in this case is git commit which commits your changes to the repository. The `-a` flag indicates that you want to "stage" all of your changes to the repository. The `-m` flag indicates that you are adding a message to your commit which is indicated in the `""` immediately after the flag.

5. Once you have committed the change push the change to the Github server

```bash
git push
```

This will take all of the changes that you committed and push them to the server.

## Exercise 2: Branch

1. Within you repository create a new branch by typing the command below

```bash
git branch [your branch here]
```

2. To start editing using the local branch you created checkout the branch by using the command below

```bash
git checkout [your branch here]
```

3. Make the changes and commit them using the `git commit` command as outlined in Exercise 1 - Step 4
   
4. Push your local branch to the remote git server
```bash
git push -u origin [your branch here]
```

5. Navigate to the GitHub repository in your browser. You should see a message indicating your branch has a recent push. Click the "Compare & pull request" button.

![Recent Push Message](/assets/recentPush.JPG)

- If the message doesn't appear navigate to the "Pull requests tab" and then create a pull request

6. This will open a pull request. Make sure to add a title and description outlining the changes you made.

![Pull Request](/assets/pullRequest.JPG)

7. Once you have create the pull request you can merge the branch into the main repository branch. This should be done by the creator of the repository. We suggest the creator share their screen and walk through the steps as a group. In the files changed tab on the right the changes that will be merged can be viewed. Review the changes, add comments under the Conversation tab, and then merge the pull request using the "Merge pull request button"

![Pull Request Merge](/assets/pullRequestMerge.JPG)


## Exercise 3: Conflicts and Merging

1. The changes will be successful for the first member of your group. The next members of your group will encounter an error pushing to Github because there will be a merge conflict. To identify the conflict run the pull command below.

```bash
git pull
```

When running the pull command git will add conflict markers to show you where the conflict is. These are identified using conflict markers `<<<<<<<`, `=======`, `>>>>>>>`. Fix the conflicts, remove the conflict markers and make another commit.

2. To merge the changes from your latest commit run the merge command below

```bash
git merge
```

3. Once each team member has merged their changes move on to Exercise 2