---
title: "Software Installation Guide for Mac Users"
layout: single
permalink: /docs/modules/readings/soft-mac/
sidebar:
 nav: module1
output:
  pdf_document: default
  word_document: default
geometry: margin=2.54cm
toc: true
---

The following steps should be performed on your personal computer. If you already have R and RStudio installed skip to step 4.

1. Download R from the link [https://cran.r-project.org](https://cran.r-project.org). Click on Download R for (Mac) OS X. Choose the most up to date version R-4.3.1.pkg. Install the package by double-clicking on it and working through the prompts. Leave all default settings in the installation options. 

2. Download the free RStudio Desktop for mac from [https://rstudio.com/products/rstudio/download/](https://rstudio.com/products/rstudio/download/). Double click the downloaded .dmg file. Drag RStudio icon to the Applications folder. 

3. Verify that RStudio and R are working together by double-clicking the RStudio icon. You should see a RStudio window with three panes. 

4. If have already installed R and RStudio just open RStudio and check for any updates by following the steps below. In your console type

```r
version
```

This will show the R version you are running. If you need to update R you can use package updateR. This is the R code you will need to type in your console:

```r
install.packages('devtools') #assuming it is not already installed
library(devtools)
install_github('andreacirilloac/updateR')
library(updateR)
updateR()
```

You will then be prompted to enter your admin password. 

Another way to do it is just downloading the new version as in Step 1. Then restart your RStudio. The new R version will be loaded automatically. Then run the following command to update packages. 

```r
update.packages()
```

Also check if you have the latest version of RStudio. Just navigate to Help > Check for updates and you be redirect to the website in Step 2 if needed. 

5. Some functions in R require a “X11 server”. You can get this using XQuartz. Download the latest version from [https://www.xquartz.org](https://www.xquartz.org). Open the downloaded DMG file and then double-click on the XQuartz.pkg. Follow the installation steps. 

6. Optional for this class. Some packages in R requires compilation. Download and install Xcode (developer tools to create applications for Mac). You can download it from your App Store or use the link: [https://apps.apple.com/us/app/xcode/id497799835?mt=12](https://apps.apple.com/us/app/xcode/id497799835?mt=12). This will take a while and requires a recent version of iOS. If you are using an old mac, please skip this step.

7. Now you need to install a package manager for macOS called Homebrew. From your Terminal type (or paste) the following command:

```terminal
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

8. Install git. Since you have Homebrew this will be simple. From your Terminal use the following command:

```terminal
brew install git
```

This command you automatically update Homebrew and run the brew clean up. You also need to install git-gui, git's commit GUI and interactive history browser, use the command

```terminal
brew install git-gui
```

Make sure to set Git with your name and email address using the following commands on the Terminal with your name and email address.

```terminal
git config --global user.name "username" <br>
git config --global user.email "email@example.com"
```

9. R has functions tied to latex. And we will use them in this class to generate pdf files. You will need to install MacTex. Download MacTeX.pkg from [https://tug.org/mactex/mactex-download.html](https://tug.org/mactex/mactex-download.html). Double-click the pkg installer and follow the prompts. Leave all default settings in the installation options. This will also take a while!


And you are all set! Your computer is ready to do run any packages and functions you will need for this class. 




