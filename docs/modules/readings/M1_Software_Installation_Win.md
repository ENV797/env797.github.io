---
title: "Software Installation Guide for Windows Users"
layout: single
permalink: /docs/modules/readings/soft-win/
sidebar:
 nav: module1
output:
  pdf_document: default
  word_document: default
geometry: margin=2.54cm
toc: true
---

This material was adapted from ENV 872 - Environmental Data Analytics and developed by Prof. John Fay.

## R

If you already have R installed, please ensure you are using version 4.3.1. If not, follow the instructions below. If you do not have R installed, follow the instructions below.

1. Open a web browser and naviate to the Duke CRAN mirror: http://archive.linux.duke.edu/cran/
2. Please select your operating system (Mac, Windows, Linux)

>    For Windows Users: install the `base package`

## RStudio
If you already have RStudio installed, please ensure you are using version 2023.06.0. To check that you are using the most up-to-date version, go to the Help menu in RStudio and select "Check for Updates." You will be instructed to install any updates that are available.

If you do not have RStudio  installed on your computer, please do the following:

1. Open a web browser and naviate to [http://www.rstudio.com/products/rstudio/download/](http://www.rstudio.com/products/rstudio/download/)
2. Select and download the appropriate installer for your operating system (Windows, Mac, Linux)
3. Open the installer and follow the onscreen directions


## Git
If you already use Git, please ensure you are using the most up-to-date version.
If you do not have Git yet installed, please do the following:

1. Open a web browser and naviate to [https://git-scm.com/download/](https://git-scm.com/download/)
2. Select and download the appropriate installer for your operating system (Windows, Mac, Linux)
3. Open the installer and follow the onscreen directions.


> **On Windows**: 
> 
> Use all the of the installation defaults **except** chosing `Notepad++` as your default Git editor. 
  

During installation, you will be asked how to configure the line-ending conversions
 
> **On Windows**: We recommend "Checkout Windows-style, commit Unix-style line endings"


## GitHub

1. Sign up for a GitHub account at [https://github.com](https://github.com). Use your Duke email address.
2. (OPTIONAL) Sign up for a GitHub Student Pack at [https://education.github.com/pack](https://education.github.com/pack) if you would like your repositories to be private. The default for repositories is public.
3. (OPTIONAL) We will be using the https protocol to clone repositories. Another option is to use SSH keys, which is a more secure option. For a guide on how to generate your own SSH key(s), see the guide from the Duke Library: https://git-rfun.library.duke.edu/outline.html.
    
## LaTeX
LaTeX will be used by RStudio and the R package `Knitr` to convert our RMarkdown files (.Rmd) into professional-quality PDF files. 
If you do not have LaTeX installed on your computer, please do the following: 

**On a PC**:

1. Install Basic MiKTeX: http://miktex.org/download.
2. Note: you need to use the MiKTeX package manager to download required style guides. 

By default, RStudio uses style guides to format our PDF documents. 
These style guides include framed.sty and titling.sty.
We have found that not all LaTeX installations include these style guides.
If you do not have them, you will get an error message when you "Knit".
To fix this, you need to install the required files.

**On a PC**:
You have two options:
  
> 1. Open the MikTeX package manager from Start.
> 2. Search for and install the following: framed, titling
>     
>     OR
>   
> 1. Type the following in command line (or GitBash):
> ```sh        
> mpm --install framed
> mpm --install titling
> ```

If your RMarkdown documents are not knitting properly, try the following troubleshooting option: 
Go to the Start menu, find the menu "MiKTeX Console", and choose the option `Always install missing packages on-the-fly`
