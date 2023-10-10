# Red Hat OpenShift Data Science Quick Course

This is the starter template for creating a new quick course in the **RedHatQuickCourses** GitHub organization. 

After you create a new repository based on this template, you need to edit and change several files and replace placeholder text and links in them.

1. Add a _README_ at the root of your repository and leave instructions for people contributing to your quick course. Make sure you provide the link to the GitHub issues page for your course so that contributors and users can report issues and provide feedback about your course.

1. Edit the **antora.yml** file in the repository root.
    * Change the _name_, _title_ and _version_ attributes
    * Edit the list of items under the _nav_ attribute to add or remove new chapters/modules to the course.

1. Edit the antora-playbook.yml file in the repository root.
    * Edit only the _title_ and _start_page_ attributes in this file. You may not be required to change the other attributes unless the need arises. 

1. Edit the _supplemental-ui/partials/header-content.hbs_ file and change the link in the _navbar-item_ div to point to the GitHub issues page for your repository.

1. Edit the files and folders under the _modules_ folder to structure your course content into chapters/modules and sections.

1. Take a brief look at the GitHub actions configuration in the _.github_ folder. It contains basic configuration to auto-generate HTML from the asciidoc source and render it using GitHub pages. Unless you know what you are doing with this, and have prior experience with GitHub actions workflows, do not change these files.

## Problems and Feedback
If you run into any issues, report bugs/suggestions/improvements about this template here - https://github.com/RedHatQuickCourses/course-starter/issues
