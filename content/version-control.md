## Version control for research using git

#--
#### What's `git`?

<img style="float: left; width: 35%" alt="xkcd 1597: git" src="img/vc/xkcd1597_git.png"/>

<div style="clear: left; font-size: 50%;">

Image: [xkcd.com/1597](https://xkcd.com/1597/)

</div>

#--
#### What's `git`?

<!-- <img style="float: left; width: 50%; background: white;" alt="Distributed version control system" src="img/vc/Distributed_VCS.png"/> -->

<div class="left">

- Version control software

- Flexible and lightweight design

- Distributed system
  - Each copy of a <code>git</code>-managed project contains all the information it needs to stand alone

</div>


#--
#### Aside: what's GitHub?

<div style="float: left; width: 35%;">
<a src="https://github.com">
<img style="vertical-align:middle;background-color:white" src="img/vc/GitHub_Logo.png" />
</a>

<a src="https://bitbucket.org">
<img style="vertical-align:middle" src="img/vc/bitbucket-logo-blue.png" />
</a>

<a src="https://about.gitlab.com">
<img style="vertical-align:middle" src="img/vc/gitlab_wm_no_bg.png" />
</a>
</div>

<div style="float: right; width: 55%">

- Hosting services for <code>git</code> repositories

- Collaboration/code sharing

- Public and private repositories
</div>

<!--<span class="footnote">For unrestricted private repositories on GitHub, sign up at https://education.github.com</span>-->


#--
#### Motivation: why use version control?

Motivation is clear for software development:

- Many developers working on large code base

- Need to keep track of changes throughout development lifecycle


#--
#### Motivation: why use version control?

But using <code>git</code> also makes sense for research programmers...

- Document development of research software

- Collaborate with supervisor or collaborators

- Track versions corresponding to key checkpoints **i.e. reproducible research**

#--
#### Motivation: why use version control?


<div class="pull-left">

**Pros**

- Track your changes
- Clean workspace
- Archive
- Experiment
- Access your work
- Share your work
- Collaborate

<!-- - Reproducible research -->
</div>

<div class="pull-right">

**Cons**

- Learning curve
- Discipline!
- Conflict resolution

</div>

#--

#### Version control basics

- A <code>git</code> project is simply a directory with some hidden files for bookkeeping

- You tell <code>git</code> which files to manage

- Three representations of file state in <code>git</code>:
  * modified files
  * staged files (index)
  * committed files (<code class="inline">HEAD</code>)

#--
#### Version control basics

<div class="splash">
Modify files in the working directory

<img style="width: 50%" src="img/vc/git_states-1.png" alt="Files in the working directory" />
</div>

#--
#### Version control basics

<div class="splash">
Stage files to the index<br/>

<img style="width: 50%" src="img/vc/git_states-5.png" alt="Files staged to the index" />
</div>

#--
#### Version control basics

<div class="splash">
Commit files (<code class="inline">HEAD</code> = most recent commit)

<img style="width: 50%" src="img/vc/git_states-6.png" alt="Committed files" />
</div>

#--
#### Version control basics

<div class="splash" style="position: relative;">
<img class="fragment" data-fragment-index="1" style="width: 50%;position:absolute;" src="img/vc/git_snapshots-1.png" alt="Git snapshots/HEAD" />
<img class="fragment fade-in" data-fragment-index="2" style="width: 50%;" src="img/vc/git_snapshots-2.png" alt="Git snapshots/HEAD" />
</div>

<ul>
<li class="fragment fade-in" data-fragment-index="1"><code class="inline">HEAD</code> references the most recently committed changes</li>
<li class="fragment fade-in" data-fragment-index="2"><code class="inline">git commit</code> adds a new link to the chain of commits</li>
</ul>

#--
#### Basic workflow

<dl>
<dt>
Inspect your workspace
</dt>
<dd>What changes have you made?</dd>

<dt>Stage files</dt>
<dd>Which changes do you want to record?</dd>

<dt>Commit files</dt>
<dd>Document and record changes</dd>

<dt>Push files</dt>
<dd>Share to remote repository</dd>

<dl>

#--
#### Best practice

- Commit code that works

- Write informative log messages

- Be aware of public vs. private repositories

- Communicate with collaborators to avoid clashes

- Use it for reproducible research and documents


#--
### Practical

<!-- #### Preliminaries -->

<!-- - Install <code>git</code> -->
<!-- - Sign up for an account on GitHub -->
<!-- - (Optional) Make sure that RStudio is ready to use git -->

#### Introduction to version control for research

[**http://bit.ly/intro-vcr**](http://bit.ly/intro-vcr)

- Using <code>git</code> on the command line
- Using <code>git</code> through RStudio

#--
### Resources

#### Documentation

- <code class="inline">git help &lt;command&gt;</code>

#--
### Resources
#### Cheatsheets and tutorials

- git - the simple guide [rogerdudler.github.io/git-guide](http://rogerdudler.github.io/git-guide/)
- Happy Git and GitHub for the useR [happygitwithr.com](https://happygitwithr.com/)
- Using Version Control with RStudio [support.rstudio.com](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN)
- oh shit, git! [ohshitgit.com](https://ohshitgit.com/)

#--
### Resources
#### Reference

- [Pro git book: **git-scm.com/book**](https://git-scm.com/book/en/v2)
- [git reference: **git-scm.com/docs**](https://git-scm.com/docs)

#--
### Configuration

<!-- TODO simple git config here (but include pointers to usethis for R users?) -->
Configure `git`:

```{r eval=FALSE, tidy=FALSE}
# set global user.name and user.email
usethis::use_git_config(user.name = "Jane Dee",
                        user.email = "janedee@example.org")
```

Initialise `git` repository and create initial commit:
```{r eval=FALSE, tidy=FALSE}
usethis::use_git(message)
```

Set up a GitHub personal access token (PAT) to allow creation/modification of GitHub repositories:
```{r eval=FALSE, tidy=FALSE}
usethis::browse_github_token()
```

Create GitHub repository associated with your project:
```{r eval=FALSE, tidy=FALSE}
usethis::use_github()
```
