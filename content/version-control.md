<!-- .slide: id="versioncontrol" -->
## Version control

#--

### Introduction to version control for research

<img style="float: left; width: 35%" alt="xkcd 1597: git" src="img/vc/xkcd1597_git.png"/>

<div style="float:left; width: 60%; padding-left: 5%">

#### What's `git`?

- Version control software <!-- .element class="fragment fade-in" -->
- Distributed system <!-- .element class="fragment fade-in" -->
  - Each copy of a project contains all the information it needs to stand alone <!-- .element class="fragment fade-in smaller" -->
- Suitable for tracking code and text-based formats <!-- .element class="fragment fade-in" -->

</div>

<div style="clear: left; font-size: 50%;">

Image: [xkcd.com/1597](https://xkcd.com/1597/)

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


#--
#### Motivation: why use version control?

Motivation is clear for software development:

- Many developers working on large code base <!-- .element class="fragment fade-in" -->
- Need to keep track of changes throughout development lifecycle <!-- .element class="fragment fade-in" -->


#--
#### Motivation: why use version control?

But using <code>git</code> also makes sense for research programmers...

- Document development of research software<!-- .element class="fragment fade-in" -->
- Share code with supervisor or collaborators<!-- .element class="fragment fade-in" -->
- Track versions corresponding to key checkpoints i.e. reproducible research <!-- .element class="fragment fade-in" -->

#--
#### Motivation: why use version control?


<div class="pull-left">

**Pros** <!-- .element class="fragment fade-in" -->

- Track your changes <!-- .element class="fragment fade-in" -->
- Clean workspace <!-- .element class="fragment fade-in" -->
- Archive <!-- .element class="fragment fade-in" -->
- Experiment <!-- .element class="fragment fade-in" -->
- Access your work <!-- .element class="fragment fade-in" -->
- Share your work <!-- .element class="fragment fade-in" -->
- Collaborate <!-- .element class="fragment fade-in" -->
- Reproducibility <!-- .element class="fragment fade-in" -->

</div>

<div class="pull-right">

**Cons** <!-- .element class="fragment fade-in" -->

- Learning curve <!-- .element class="fragment fade-in" -->
- Discipline! <!-- .element class="fragment fade-in" -->
- Conflict resolution <!-- .element class="fragment fade-in" -->

</div>

#--

#### Version control basics

<ul>
<li class="fragment fade-in">
A <code>git</code> project is simply a directory with some hidden files for bookkeeping
</li>
<li class="fragment fade-in">
You tell <code>git</code> which files to manage
</li>
<li class="fragment fade-in">
Three representations of file state in <code>git</code>:
<ul>
<li>modified files</li>
<li>staged files (changes you want to record)</li>
<li>committed files (latest record of changes)</li>
</ul>
</li>
</ul>

#--
#### Version control basics

<div class="splash" style="position:relative">

<div class="fragment fade-in-then-out" data-fragment-index="1" style="position:absolute">
Modify files in the working directory

<img style="width: 50%" src="img/vc/git_states-1.png" alt="Files in the working directory" />
</div>

<div class="fragment fade-in-then-out" data-fragment-index="2" style="position:absolute">
<!-- Stage files to the index -->
Choose files to include in snapshot
<br/>
<img style="width: 50%" src="img/vc/git_states-5.png" alt="Files staged to the index" />
</div>

<div class="fragment" data-fragment-index="3" style="position:absolute">
<!-- Commit files (<code class="inline">HEAD</code> = most recent commit) -->
Create snapshot of project
<br/>
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
</dt> <!-- .element class="fragment fade-in" -->
<dd>What changes have you made?</dd> <!-- .element class="fragment fade-in" -->

<dt>Stage files</dt> <!-- .element class="fragment fade-in" -->
<dd>Which changes do you want to record?</dd> <!-- .element class="fragment fade-in" -->

<dt>Commit files</dt> <!-- .element class="fragment fade-in" -->
<dd>Document and record changes</dd> <!-- .element class="fragment fade-in" -->

<dt>Push files</dt> <!-- .element class="fragment fade-in" -->
<dd>Share to remote repository</dd> <!-- .element class="fragment fade-in" -->

<dl>

#--
#### Best practice

- Commit code that works <!-- .element class="fragment fade-in" -->
- Write informative log messages <!-- .element class="fragment fade-in" -->
- Be aware of public vs. private repositories <!-- .element class="fragment fade-in" -->
- Communicate with collaborators to avoid clashes <!-- .element class="fragment fade-in" -->
- Use it for reproducible research and documents <!-- .element class="fragment fade-in" -->


#--
#### Version control for data?

- Version control is not suited for datasets!
  - Including large binary files clogs up your repository
  - Hosting service restrictions on file sizes
  - License restrictions on redistributing data

- Deposit data with a suitable <a href="#/datasharing">data repository</a> instead

- Record which data version was used in your analysis scripts


#--
#### More about version control

- Often delivered in December

- <em>Version control with Git</em>, CEMAC training session<br/>
<span style="font-size:70%">Email <a href="mailto:cemac-support@leeds.ac.uk?subject=CEMAC%20Training">cemac-support@leeds.ac.uk</a> with subject &ldquo;CEMAC Training&rdquo; to sign up</span>

- <em>Introduction to version control for research</em><br/>
<a href="http://bit.ly/intro-vcr">http://bit.ly/intro-vcr</a>


#--
### Resources
#### Summary Guides and Tutorials

<div class="smaller">

- git - the simple guide [rogerdudler.github.io/git-guide](http://rogerdudler.github.io/git-guide/)
- Happy Git and GitHub for the useR [happygitwithr.com](https://happygitwithr.com/)
- Using Version Control with RStudio [support.rstudio.com](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN)
- oh dangit, git! [dangitgit.com](https://dangitgit.com/)

</div>

#### Reference

<div class="smaller">

- Pro git book: [**git-scm.com/book**](https://git-scm.com/book/en/v2)
- git reference: [**git-scm.com/docs**](https://git-scm.com/docs)

</div>

### PAUSE here


<!-- #-- -->
<!-- ### Configuration -->

<!-- <\!-- TODO simple git config here (but include pointers to usethis for R users?) -\-> -->
<!-- Configure `git`: -->

<!-- ```{r eval=FALSE, tidy=FALSE} -->
<!-- # set global user.name and user.email -->
<!-- usethis::use_git_config(user.name = "Jane Dee", -->
<!--                         user.email = "janedee@example.org") -->
<!-- ``` -->

<!-- Initialise `git` repository and create initial commit: -->
<!-- ```{r eval=FALSE, tidy=FALSE} -->
<!-- usethis::use_git(message) -->
<!-- ``` -->

<!-- Set up a GitHub personal access token (PAT) to allow creation/modification of GitHub repositories: -->
<!-- ```{r eval=FALSE, tidy=FALSE} -->
<!-- usethis::browse_github_token() -->
<!-- ``` -->

<!-- Create GitHub repository associated with your project: -->
<!-- ```{r eval=FALSE, tidy=FALSE} -->
<!-- usethis::use_github() -->
<!-- ``` -->
