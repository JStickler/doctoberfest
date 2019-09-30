# Contributor's Guide Template

Documentation is an integral part of any open source project.  But every project is different. This template is designed to assist you in creating a contributors guide specifically for documentation contributions to your project.

The overlap between writers and developers is small.  If you're a developer you may look at some of the information in this template and think, "But people should already know that."  There are a lot of writers out there who might like to contribute to documentation, but they don't know how to get started.  Our goal is to make it as easy as possible for anyone to make documentation contributions to an open source project.

## Simple Edits

GitHub makes it easy for _anyone_ to make small documentation edits, like fixing a typo.  You don't need to install any tools, all you need is access to GitHub and a browser.  This procedure works best when you want to make small changes to an existing file.

NOTE: You must have a [GitHub account](https://github.com/join) to make or propose changes to a project.

1. Log into your GitHub account.
2. In the GitHub repository, navigate to the file you want to edit.
3. Click the file name to open it in GitHub.
4. Click the pencil (edit icon) near the top right of the page contents. GitHub opens an editing page with the following message:
```
 You’re editing a file in a project you don’t have write access to. We’ve created a fork of this project for you to commit your proposed changes to. Submitting a change to this file will write it to a new branch in your fork, so you can send a pull request.
```
5. Make your edits.
6. Enter a title and description of your changes in the **Propose File Changes** section at the bottom of the page. Enter enough detail so that the project maintainers to know what you have changed and why.
7. Enter your e-mail address.
8. Click the **Propose file change** button.

Community members will review your changes and if they agree with them, they will merge them into the project.  Since community members are volunteers, this may take some time.  Be patient, and thank you for your contribution!

## Files and layout

How are files arranged in your documentation project?  Even if someone is going to make an edit through the Web interface, they still need to be able to find the file in your project.

* Where can you find the content (text) files?
* Where should you store images and graphics?
* Is there a variable or attributes file?
* Is there a topic map?
* Is there a folder for shared content such as snippets or common files?
* Is there a folder for code samples?

Sometimes drawing a map of your directory structure can be helpful.  For example:
```
├── README.md
├── content (All content files here)
│   ├── api (API documentation)
│   ├── install (installation documentation)
│   ├── configure (configuration information)
│   ├── dev (developer guide)
│   ├── user (user guide)
├── images (all graphics and images)
├── scripts (scripts for the project)
├── templates (page or topic templates)
├── themes (style sheets for the project)
```


## Tools

If you want to change more than one file, or write new content, you're going to need to install the tools used by the project to create their documentation.

Things to include in this section include, what markup language are you using to create your documentation files?  Include links to cheat sheets for people who may need to refresh their memory.  For example:

* [markdown](https://www.markdownguide.org/) (Specify which variety? [CommonMark](https://commonmark.org/), [GitHub flavored](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), etc.)
* [asciidoc](https://asciidoctor.org/docs/asciidoc-syntax-quick-reference/)
* [HTML](https://www.w3schools.com/html/)


What tools are you using to generate your output?  Include links to downloads.  For example:

* [GitHub Pages](https://pages.github.com/)
* [Hugo](https://gohugo.io/)
* [Jekyll](https://jekyllrb.com/)

Do your tools have dependencies? For example:

* [Asciidoctor](https://asciidoctor.org/)
* [Python](https://www.python.org/)
* [Ruby](https://www.ruby-lang.org/en/)

## Setting up Git

Most non-developers may not have experience with Git, but still want to contribute to the documentation.  Help them out by providing links and explicit instructions for how to get started with Git.  Remember, this is about making it as easy as possible for newcomers and Git can be challenging even if you have experience with it.

GitHub provides a set of [Git cheatsheets](https://github.github.com/training-kit/) in multiple languages.

1. First [Install Git](https://help.github.com/en/articles/set-up-git)

2. Perform the initial Git setup tasks, as described in [First Time Git Setup](link:https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).

3. Navigate to the GitHub repository and [create a fork](https://help.github.com/en/articles/fork-a-repo). This will create your own version of the repository which you can find at https://github.com/{yourusername}/{project-name} where {yourusername} is the username you created in GitHub.

4. [Clone](https://help.github.com/en/articles/cloning-a-repository) from your fork to create a copy on your local machine.

  NOTE: It is possible to clone using SSH so you don't have to enter a username/password every time you push. Find instructions at [Connecting to GitHub with SSH](https://help.github.com/articles/connecting-to-github-with-ssh/) and [Which Remote URL Should I Use](https://help.github.com/articles/which-remote-url-should-i-use/). When using SSH, the origin lines will appear like this:
`git@github.com:{yourusername}/{project-name}.git`


```
$ git clone https://github.com/{yourusername}/{repository-name}
```

5. Navigate to the new directory by entering the following from the command line on your local machine:
```
$ cd {repository-name}
```

6. Add a git remote to your local repository to link to the upstream version of the documentation. This makes it easier to update your fork and local version of the documentation.
```
$ git remote add upstream https://github.com/{project-name}
```

7. Check your settings.
```
$ git remote -v
origin    https://github.com/{YOUR_USERNAME}/{YOUR_FORK}.git (fetch)
origin    https://github.com/{YOUR_USERNAME}/{YOUR_FORK}.git (push)
upstream  https://github.com/{ORIGINAL_OWNER}/{ORIGINAL_REPOSITORY}.git (fetch)
upstream  https://github.com/{ORIGINAL_OWNER}/{ORIGINAL_REPOSITORY}.git (push)
```

## Contributing

Other things to think about including in your documentation contributor's file:

* Does your project have [templates](https://github.com/redhat-documentation/modular-docs) specifically for documentation?
* Does your project have a file naming convention?
* Does your project have a style guide?
* Does your project have screenshot or graphics standards?  A preferred graphics file format (.png, .svg)?
* What are the processes for reviewing content submissions?
* Do contributors need to sign their PRs?
* Does your project have any guidelines around https://chris.beams.io/posts/git-commit/[commit messages]?


## Links

Here are some other links that may be helpful as you're creating your documentation contributor's file.

[How to contribute to Open Source](https://opensource.guide/how-to-contribute/) from Open Source Guides.

[Contributor's Guide for Open Source Guides](https://github.com/github/opensource.guide/blob/master/CONTRIBUTING.md)

The Red Hat documentation team has started publishing resources to a [public repository](https://github.com/redhat-documentation).

The [OpenJDK documentation](https://github.com/red-hat-openjdk/docs) has a good example contributor's guide.

The  [Keycloak documentation](https://github.com/keycloak/keycloak-documentation) also has a good example contributor's guide.

YCombinator [thread about contributor's files with links](https://news.ycombinator.com/item?id=4828165)

Mozilla Science lab [article about building a contributor's file](https://mozillascience.github.io/working-open-workshop/contributing/)

[GitLab documentation contributor's file](https://about.gitlab.com/community/contribute/documentation/)

[Fedora documentation contributor's guide](https://docs.fedoraproject.org/en-US/fedora-docs/)

[Hugo contributor's guide](https://gohugo.io/contribute/documentation/)
