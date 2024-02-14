---
title: "Integrating Git and RStudio"
layout: single
permalink: /docs/modules/readings/gitsetup/
sidebar:
 nav: module1
output:
  pdf_document: default
  word_document: default
geometry: margin=2.54cm
toc: true
---


## Registering a GitHub account

You will need to create a free GitHub account. Navigate to [https://github.com](https://github.com), click the Sign Up button, and follow the instructions to set up a free account. Note that if you already have an account you don't to register for a new one.

## Forking and Cloning 

1. Go to the following [class repository](https://github.com/ENV797/TSA_Sp24) on GitHub.

2. Sign in (via the button in the upper right corner). 

3. In the upper right corner, click the "fork" button. This will prompt you to create a copy of the class repository in your own user account. See image below. This is called a fork of the original repository, which you can edit rather than simply download. 

![Screenshot](/docs/assets/git-fork.jpeg)

4. Clone your repository to your local drive using RStudio. <br>

 * Copy the GitHub repository URL of your cloned repository - not the main class repository. <br>

 * Click the green "Code" button to expose the Clone sub-menu. With the `HTTPS` option selected, click the :clipboard: icon which copies the forked repsository's URL to your clipboard. <br>

 ![Screenshot](/docs/assets/git-clone.jpeg)

 * Launch RStudio and select "New Project" from the File menu. Choose "Version Control" and "Git." <br>

 ![Screenshot](/docs/assets/R-newproj.jpeg)

 * Paste the repository URL and give your repository a name and a file path (i.e. a local folder where you want to store the file in your computer). The file path should be one that persists permanently, i.e., either on the course server for lab computers or a dedicated space on your personal computer. <br>

You now have tracked the course repository (i.e., the "upstream"), forked the repository into your own account (i.e., the "remote"), and cloned the repository to your drive (i.e., the "local"). We will be updating each of these repositories as the course progresses. <br>

Note: Clone with SSH is an option as well. For a guide on creating SSH keys, see the Duke Libraries online guide here and navigate to the "Generate SSH keys" section:  https://git-rfun.library.duke.edu/outline.html#generate_ssh_keys_in_advance_of_the_workshop. <br>

## Adding your GitHub credentials to your local repository

In RStudio, activate the Git menu, and from this menu click the :gear: icon, and select the `Shell...` option. This will open up the Git Bash shell for this repository.

  ![Screenshot](/docs/assets/R-git-shell.jpeg)

At the shell prompt type the following two commands to set you repository's user name and email, replacing my Git username and email with the username and email associated with your GitHub account:

  ![Screenshot](/docs/assets/R-terminal.jpeg)

```terminal
git config user.name 'yourusername'
git config user.email 'youremail'
```

## Creating you personal access token

To facilitate repository management on GitHub, you will need to create a "personal access token" that grants your local machine the necessary permissions to upload new and modified files to your repository. Follow these steps to generate your personal access token:

1. Ensure that you are logged in to your personal GitHub account.
2. Navigate to the following link: [https://github.com/settings/tokens](https://github.com/settings/tokens).
3. Select "Generate new token (classic)." You might need to re-authenticate for security purposes.
4. During the token creation, configure the settings as follows:
* Add a descriptive note to help identify the token's purpose (e.g., "ENV 797").
* Set the expiration date to a time beyond the semester's conclusion.
* For scopes, check the following boxes: repo, workflow and user
5. Click on "Generate token" to finalize the process.
6. **Copy the generated token and store it in a secure location**. This step is crucial, as you'll need it to link any new RStudio session to your GitHub account and Github will not display the token again. 

This token serves as a secure and temporary credential for your local machine, enabling seamless interactions with your GitHub repository throughout the semester.

## Add you Personal Access Token (PAT) to RStudio

Go to the Console window in RStudio - not the Terminal. Console shoudl be next to the Terminal tab as shown in the image below.

  ![Screenshot](/docs/assets/R-console.jpeg)

1. Install the “usethis” package with the following command:

```r
install.packages("usethis")
```
2. Then run following command to save your PAT as a Git credential:

```r
gitcreds::gitcreds_set()
```
This will start a set of prompts asking you to save your PAT as an encrypted file on the local machine. Paste the token you copied on step 6 of "Creating your Own Personal Token" and you are all set.



