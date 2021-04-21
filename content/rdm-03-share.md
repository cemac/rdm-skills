<div class="splash">
<img src="img/data_lifecycle_share.png" width="30%" />
</div>

#--

## Version control

#--

### Introduction to version control for research

<img style="float: left; width: 35%" alt="xkcd 1597: git" src="img/vc/xkcd1597_git.png"/>

<div style="float:left; width: 60%; padding-left: 5%">

#### What's `git`?

<ul>
<li class="fragment fade-in">
Version control software
</li>
<!-- <li class="fragment fade-in"> -->
<!-- Flexible and lightweight design -->
<!-- </li> -->
<li class="fragment fade-in">
Distributed system
<ul>
<li style="font-size:smaller">Each copy of a <code>git</code>-managed project contains all the information it needs to stand alone</li>
</ul>
</li>
<li class="fragment fade-in">
Suitable for tracking code and text-based formats
</li>
</ul>

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

<ul>
<li>
Motivation is clear for software development:

<ul>
<li class="fragment fade-in">
Many developers working on large code base
</li>
<li class="fragment fade-in">
Need to keep track of changes throughout development lifecycle
</li>
</ul>

</li>
</ul>

#--
#### Motivation: why use version control?

<ul>
<li>
But using <code>git</code> also makes sense for research programmers...

<ul>
<li class="fragment fade-in">
Document development of research software
</li>
<li class="fragment fade-in">
Share code with supervisor or collaborators
</li>
<li class="fragment fade-in">
Track versions corresponding to key checkpoints i.e. <strong>reproducible research</strong>
</li>
</ul>

</li>
</ul>

#--
#### Motivation: why use version control?


<div class="pull-left fragment fade-in">

**Pros**

<ul>
<li class="fragment fade-in">
Track your changes
</li>
<li class="fragment fade-in">
Clean workspace
</li>
<li class="fragment fade-in">
Archive
</li>
<li class="fragment fade-in">
Experiment
</li>
<li class="fragment fade-in">
Access your work
</li>
<li class="fragment fade-in">
Share your work
</li>
<li class="fragment fade-in">
Collaborate
</li>
<li class="fragment fade-in">
Reproducibility
</li>
</ul>
</div>

<div class="pull-right fragment fade-in">

**Cons**

<ul>
<li class="fragment fade-in">
Learning curve
</li>
<li class="fragment fade-in">
Discipline!
</li>
<li class="fragment fade-in">
Conflict resolution
</li>
</ul>

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
<li>staged files (index)</li>
<li>committed files (<code class="inline">HEAD</code>)</li>
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
Stage files to the index
<br/>
<img style="width: 50%" src="img/vc/git_states-5.png" alt="Files staged to the index" />
</div>

<div class="fragment" data-fragment-index="3" style="position:absolute">
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
#### Version control for data?

- Version control is not suited for large datasets!
  - Data is not expected to change frequently/at all
  - Restrictions on file sizes
  - Restrictions on redistributing data
  
- Deposit data with a suitable **data repository** instead

- Record which data version was used in your analysis scripts

  


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

## Data repositories


#--

### Why use a data repository?

- Publish versioned data for re-use
- May be requirement of your funder
- Assign digital object identifiers (DOIs)
  - Permanently identify your work
  - Means to cite specific datasets
- Provide stable long-term access to data
- Metadata enable search within data repositories


#--

### General data repositories

- [Figshare](http://figshare.com/)
- [Dryad](https://datadryad.org/stash)
- [Open Science Framework](https://osf.io/)
- [Zenodo](https://zenodo.org/)

#--

### Specialist data repositories

- Organisation specific repositories e.g. [Research Data Leeds Repository](https://archive.researchdata.leeds.ac.uk/)
- Domain specific data centres e.g. [EIDC](https://www.ceh.ac.uk/data/nerc-data-centre "Environmental Information Data Centre"), [BODC](https://www.bodc.ac.uk/ "British Oceanographic Data Centre"), [CEDA Archive](https://archive.ceda.ac.uk/ "Centre for Environmental Data Analysis (CEDA) Archive")

#--

### Choosing a data repository

- Check guidance from your institution
- Check requirements from your funder (including licensing)
- Check usage restriction/charges e.g. limits on data upload and storage


#==

<div class="splash">
<img src="img/data_lifecycle_archive.png" width="30%" />
</div>

#--

## Archiving and DOIs

- Benefits of archiving your data or code
  - Long term reference to research outputs
  - Allows reuse and adaptation (subject to license)
  - Assigning a DOI means that outputs can be easily cited and located

#--

#### Example: manual upload via [Zenodo](https://zenodo.org/)

- Upload type: dataset, source code etc
- Reserve DOI so that you can include it in linked research outputs such as published papers
- Metadata including licensing and funding information


#--

#### Example: [Zenodo](https://zenodo.org/) and GitHub

- Link Zenodo and GitHub accounts
- Create GitHub release
- Register an associated DOI

#==

<div class="splash">
<img src="img/data_lifecycle_re-use.png" width="30%" />
</div>

#--

## FAIR data principles

<dl>
<dt>Findable</dt>
<dd>Unique identifiers and metadata allow data to be located quickly and efficiently</dd>
<dt>Accessible</dt>
<dd>Data can be accessed using standard protocols</dd>
<dt>Interoperable</dt>
<dd>Common or standardised interfaces allow use of data in a wide range of applications</dd>
<dt>Re-usable</dt>
<dd>Data is clearly described and includes license for reuse</dd>
</dl>
