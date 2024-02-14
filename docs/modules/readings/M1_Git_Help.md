---
title: "Version Control and Git"
layout: single
permalink: /docs/modules/readings/githelp/
sidebar:
 nav: module1
output:
  pdf_document: default
  word_document: default
geometry: margin=2.54cm
toc: true
---

This material was adapted from ENV 872 - Environmental Data Analytics and developed by Prof. John Fay.

## Version Control

**Version control** is the process by which all changes to code, text, and files are tracked. In this manner, we're also able to maintain data and information to support collaborative projects, but to also make sure your analyses are preserved.

**GitHub** is the web hosting platform for maintaining our Git repositories. Our version control system for the purposes of this course is **Git**. 

GitHub repositories come in two forms: public and private. All the project repositories you will use for this course are public. There may be situations in the future in which you may want to make use of private repositories, in which data and progress are protected from public view. Private repositories can be made public at a later date.

## Licensing

Licensing is also important to specify who and how your code can be used by others. Various license types are available for use with a decision tree available [here](https://choosealicense.com/). For the purposes of this work, we recommend a [GNU General Public License version 3](https://choosealicense.com/licenses/gpl-3.0/). This is a free and widely-trusted *copyleft* license. A copyleft is an arrangement whereby software or artist work may be used, modified, and distributed freely on condition that anything derived from it is bound by the same condition. Unless you plan to charge a fee for use of your code, the GPLv3.0 comes highly recommended.

For more information about licensing your code, check out this [link](https://help.github.com/articles/licensing-a-repository/).

## Functions in Git

There are two ways to diverge code from a main project: **branching** and **forking**
A *branch* is a temporary segment often used for development. We will not be making use of branching for the purposes of this class, but it is worth spending some time reading about them to see how they can be incorporated into collaborative projects. 
A *fork* is a copy or clone of the main project. Forking allows for greater oversight in the merging process and prevents changes being committed to the main project.  

## Editing, Committing, Pushing

1. Navigate to the "README.md" file in the Files tab and open it. <br>

2. Type your name after "Student:" and save. <br>

3. Now that you have edited a file, it should now appear in the Git tab. Click the box to the left of the file, where a check mark should now appear. <br>

4. Press the "Commit" button. A new window should appear that shows the changes that have been made to the file. <br> 

5. Write a message detailing the edits you've made to the README file. You should always include a commit message to your commits so that your future self and/or your collaborators will know what changes were made. Click "Commit".

6. Click the green upward facing arrow: the "Push" button. Your remote repository is now up to date with your local repository. 

The commit command records the changes you've made to files in your project. **Commits** are useful to track important milestones in your progress. You should always make a commit at least once every time you log onto a project (e.g., once daily). However, simply committing your changes does not save those changes to your remote repository. This is where **push** comes in. By pushing your new commits to the remote repository, you are ensuring that your local and remote repositories contain the same changes. You must have an internet connection to push, but you can make several commits offline and push them when you regain an internet connection.

Commits and pushes can also be done in the Terminal by typing commands (i.e., the command line). Navigating to the Terminal tab will allow you to type these commands. The relevant commands are: 

```terminal
git commit
git push
``````

Note: files must be staged in order to use the command `git commit`, and a commit message must still be used.

If you are using a Mac, you will need to take the following steps to enter your commit message: 

1. press "i" to indicate insert

2. write your merge message

3. press "esc" to indicate you are exiting the insertion

4. write ":wq" to indicate write then quit

5. press enter

## Pulling from the Remote

If there are changes in your remote repository that you want to incorporate into your local repository, you will need to pull them into your local repository. 

1. Click the blue downward facing arrow: the "Pull" button. Your local repository is now up to date with your remote repository. 

## Pulling from the Upstream Remote

Your instructor will regularly update the course repository. However, this will not update the repository that you've forked into your own user account (i.e., remote) unless you tell it to do so. <br>

Type the following commands into the Terminal window in RStudio (bottom left) <br>

```terminal
git remote add upstream https://github.com/ENV797/TSA_Sp24
git pull upstream main
``````

An alternate to pull is fetch + merge: <br>

```terminal
git fetch upstream main
git merge upstream
``````

Note: these steps will update your local repository, but will not update your remote. To bring your remote up to date, you will need to push your changes. <br>

Note: you will not be pushing any of your changes to the upstream remote, as you do not have the appropriate permissions to do so. <br>

## Merge

Sometimes, files in your local and remote repositories will have changes that are different. In this case, you will need to merge the files together in a way that incorporates the changes in a manner that you choose (merge). When a merge conflict occurs, you will need to open the conflicted file in RStudio, review any edits that are inconsistent across versions, and make edits to incorporate all desired updates. You may then commit and push. <br>


