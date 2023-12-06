# Introduction to Red Hat OpenShift AI

This is the first in a series of five courses about Red Hat OpenShift AI (RHOAI).
This foundational courses introduces the features, use-cases, concepts, terminology and the architecture of the product.

# Creating Course Content

We use a system called Antora (https://antora.org) to publish courses. Antora expects the files and folders in a source repository to be arranged in a certain opinionated way to simplify the process of writing course content using asciidoc, and then converting the asciidoc source to HTML.

Refer to the quick courses [contributor guide](https://redhatquickcourses.github.io/welcome/1/guide/overview.html) for a detailed guide on how to work with Antora tooling and publish courses.

## TL;DR Quickstart

This section is intended as a quick start guide for technically experienced members. The contributor guide remains the canonical reference for the course content creation process with detailed explanations, commands, video demonstrations, and screenshots.

### Pre-requisites

* You have a macOS or Linux workstation. Windows has not been tested, or supported. You can try using a WSL2 based environment to run these steps - YMMV!
* You have a somewhat recent version of the Git client installed on your workstation
* You have a somewhat new Node.js LTS release (Node.js 16+) installed locally. 
* Install a recent version of Visual Studio Code. Other editors with asciidoc editing support may work - YMMV, and you are on your own...

### Antora Files and Folder Structure

The *antora.yml* file lists the chapters/modules/units that make up the course.

Each chapter entry points to a *nav.adoc* file that lists the sections in that chapter. The home page of the course is rendered from *modules/ROOT/pages/index.adoc*.

Each chapter lives in a separate folder under the *modules* directory. All asciidoc source files live under the *modules/CHAPTER/pages* folder. 

To create a new chapter in the course, create a new folder under *modules*. 

To add a new section under a chapter create an entry in the *modules/CHAPTER/nav.adoc* file and then create the asciidoc file in the *modules/CHAPTER/pages* folder.

### Steps

1. Clone the course repository.
```
    $ git clone git@github.com:RedHatQuickCourses/rhods-intro.git
```

2. Install the npm dependencies for the course tooling.
```
    $ cd rhods-intro
    $ npm install
```

3. Start the asciidoc to HTML compiler in the background. This command watches for changes to the asciidoc source content in the **modules** folder and automatically re-generates the HTML content.
```
    $ npm run watch:adoc
```
4. Start a local web server to serve the generated HTML files. Navigate to the URL printed by this command to preview the generated HTML content in a web browser.
```
    $ npm run serve
```

5. Before you make any content changes, create a local Git branch based on the **main** branch. As a good practice, prefix the branch name with your GitHub ID. Use a suitable branch naming scheme that reflects the content you are creating or changing.
```
    $ git checkout -b rsriniva/ch01s01
```

6. Make your changes to the asciidoc files. Preview the generated HTML and verify that there are no rendering errors.Commit your changes to the local Git branch and push the branch to GitHub.
```
    $ git add .
    $ git commit -m "Added lecture content for chapter 1 section 1"
    $ git push -u origin rsriniva/ch01s01
```

7. Create a GitHub pull request (PR) for your changes using the GitHub web UI.

8. Request a review of the PR from your technical peers and/or a member of the PTL team.

9. Make any changes requested by the reviewer in the **same** branch as the PR, and then commit and push your changes to GitHub. If other team members have made changes to the PR, then do not forget to do a **git pull** before committing your changes.

10. Once reviewer(s) approve your PR, you should merge it into the **main** branch.

11. Wait for a few minutes while the automated GitHub action publishes your changes ot the production GitHub pages website.

12. Verify that your changes have been published to the production GitHub pages website at https://redhatquickcourses.github.io/rhods-intro

## Problems and Feedback
If you run into any issues, report bugs/suggestions/improvements about this course here - https://github.com/RedHatQuickCourses/rhods-intro/issues