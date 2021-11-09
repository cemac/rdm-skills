<div class="splash">
<img src="img/data_lifecycle_create.png" width="30%" />
</div>

#--

## Data creation and acquisition

#--

- Collecting data from field or lab work
- Acquiring data from another source or service e.g. satellite data

#--

### Field and experimental data

- Use your lab and field notes to record information that will be required for correct interpretation of the data
  - e.g. butterfly monitoring, record wind/sun
  - e.g. experimental data, record instruments and settings

#--

### Field and experimental data

- Decide how your data will be structured before you start so that you know what you need to record
- Use <a href="#/tidydata">tidy data principles</a> to structure your data

#--

### Field and experimental data

- How can you ensure quality control when entering data?
  - Carry out checks for unusual values
  - Be consistent in how you encode missing values

#--

### Field and experimental data

- When you've entered and checked your data, set file permissions to protect data from further changes

#--
<!-- .slide: id="tidydata" -->
### Tidy data principles

- Differentiate between:
  - Variables (things that you've measured for each unit)
  - Observations (all measurements for a single unit)

<span class="footnote"><a href="https://www.jstatsoft.org/article/view/v059i10">Tidy Data, Wickham, 2014, Journal of Statistical Software</a></span>

#--

### Tidy data principles

- Variables are stored in **columns**, observations are stored in **rows**

<div class="splash">
<img src="img/tidy-1.png" width="70%" />
</div>

<p class="footnote">
  Image re-used under a <a href="https://creativecommons.org/licenses/by/4.0/legalcode">CC-BY 4.0</a> license from <a href="https://the-turing-way.netlify.app/welcome.html">The Turing Way</a> community materials.
  DOI: <a href="https://doi.org/10.5281/zenodo.3233853">https://doi.org/10.5281/zenodo.3233853</a>
</p>


#--

### Tidy data principles

- Using a tidy data format makes it easy to summarise and query your data:

<dl style="font-size:smaller">
  <dt>Filter</dt>
  <dd>Choose observations</dd>
  <dt>Transform</dt>
  <dd>Calculate new values from measured variables</dd>
  <dt>Aggregate</dt>
  <dd>Create summary statistics</dd>
  <dt>Sort</dt>
  <dd>Order data by values of a given variable</dd>
</dl>

#--

#### Example: Tidy data

<span style="font-size:66%">Hourly measured PM2.5 particulate matter, Devonshire Green, Sheffield</span>

```[1-5|2|1]
|Date      |01:00 |02:00 |03:00 | ...
|01/01/2020|33.019|26.321|26.179|
|02/01/2020|12.948|9.906 |8.774 |
|03/01/2020|2.594 |2.618 |2.5   |
|04/01/2020|6.368 |5.519 |6.085 |
    .
    .
    .
```

<span class="footnote"> &copy; Crown 2021 copyright Defra via [uk-air.defra.gov.uk](uk-air.defra.gov.uk), licenced under the [Open Government Licence](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/2/) (OGL) </span>


#--

#### Example: Tidy data

<span style="font-size:66%">Hourly measured PM2.5 particulate matter, Devonshire Green, Sheffield</span>

```[1-4,6-8,10-12,14-16|2|3|4|2-5|2,6,10,14]
|Date      |Time |PM2_5 |
|01/01/2020|01:00|33.019|
|01/01/2020|02:00|26.321|
|01/01/2020|03:00|26.179|
|...       |...  |...   |
|02/01/2020|01:00|12.948|
|02/01/2020|02:00|9.906 |
|02/01/2020|03:00|8.774 |
|...       |...  |...   |
|03/01/2020|01:00|2.594 |
|03/01/2020|02:00|2.618 |
|03/01/2020|03:00|2.5   |
|...       |...  |...   |
|04/01/2020|01:00|6.368 |
|04/01/2020|02:00|5.519 |
|04/01/2020|03:00|6.085 |
|...       |...  |...   |
```

<span class="footnote"> &copy; Crown 2021 copyright Defra via [uk-air.defra.gov.uk](uk-air.defra.gov.uk), licenced under the [Open Government Licence](http://www.nationalarchives.gov.uk/doc/open-government-licence/version/2/) (OGL) </span>


#--

### Data from an external source

<ul>
  <li>
    What is the interface for accessing data?
    <ul>
      <li><a href="https://www.ncei.noaa.gov/data/global-forecast-system/access/grid-004-0.5-degree/forecast/202111/20211106/">Remote access</a> e.g. FTP or HTTP <!-- Example NOAA recent data -->
        <ul>
          <li>Access via FTP client or web browser</li>
          <li>Automate using command line scripting</li>
        </ul>
      </li>
      <li><a href="https://www.ncei.noaa.gov/has/HAS.FileAppRouter?datasetname=GFSGRB24&subqueryby=STATION&applname=&outdest=FILE">Order form on website</a></li>
      <li><a href="https://www.metoffice.gov.uk/services/data/datapoint/about">Web API based access</a> <!-- Example: Met Office DataPoint -->
        <ul>
          <li>Register for API key</li>
          <li>Submit URL based query to access data</li>
          <li>Data served in XML/JSON format</li>
          <li>Fair use policy</li>
        </ul>
      </li>
    </ul>
  </li>
</ul>


#--

### Data from an external source

<ul>
<li>How long will it take to get the data that you need?
  <ul>
    <li>Time to process order request</li>
    <li>
      Download times
    </li>
  </ul>
</li>
<li>
  Be aware of service limitations
  <ul>
    <li>
      Data size restrictions
    </li>
    <li>
      Potential latency when accessing archived data
    </li>
  </ul>
</li>
<li>Be alert to changes in data format/contents</li>
</ul>

#--

### Data from an external source

- What are the licensing terms?
  - Check license for any restrictions or requirements for use of data
- How much space do you need to store the data?

#--

## Organising and describing your data<br/>

#--

<ul>
  <li>Working to accepted standards will make your data easier to understand
    <ul>
      <li class="fragment fade-in">
        File naming conventions</li>
      <li class="fragment fade-in">
        Directory structure</li>
      <li class="fragment fade-in">
        Describing your data using metadata</li>
      <li class="fragment fade-in">
        File formats</li>
    </ul>
  </li>
</ul>


#--

### File naming conventions

- Use file names to reflect logical order of workflows

<span class="fragment fade-in-then-out">

<pre><code data-trim data-noescape>
<span class="hljs-strong">01</span>-import_data.R
<span class="hljs-strong">02</span>-first_analysis.R
<span class="hljs-strong">03</span>-second_analysis.R
</code>
</pre>

</span>

<span class="fragment fade-in">

<pre><code data-trim data-noescape>
<span class="hljs-strong">01a</span>-import_data.R
<span class="hljs-strong">01b</span>-preprocess_data.R
<span class="hljs-strong">02</span>-first_analysis.R
<span class="hljs-strong">03</span>-second_analysis.R
</code>
</pre>

</span>

#--

### File naming conventions

<div class="left">

- Use file names to organise data or outputs

<span class="fragment fade-in">

<pre><code data-trim data-noescape>
<span class="hljs-strong">01Oct2021</span>_extended.gif
<span class="hljs-strong">01Oct2021</span>_extended_domain.png
<span class="hljs-strong">01Oct2021</span>_extended_lsta_imerg.png
<span class="hljs-strong">01Sep2021</span>_extended.gif
<span class="hljs-strong">01Sep2021</span>_extended_domain.png
<span class="hljs-strong">01Sep2021</span>_extended_lsta_imerg.png
<span class="hljs-strong">02Oct2021</span>_extended_domain.png
<span class="hljs-strong">02Oct2021</span>_extended_lsta_imerg.png
</code></pre>

</span>

</div>

#--

### File naming conventions

<div class="left">

- Use ISO 8601 format for dates in filenames: <code><span class="hljs-strong">YYYY-MM-DD</span></code> or <code><span class="hljs-strong">YYYYMMDD</span></code>

<span class="fragment fade-in">

- Ensures correct order when listing files

<span class="fragment fade-in">

<pre><code data-trim data-noescape>
<span class="hljs-strong">2021-09-01</span>_extended.gif
<span class="hljs-strong">2021-09-01</span>_extended_domain.png
<span class="hljs-strong">2021-09-01</span>_extended_lsta_imerg.png
<span class="hljs-strong">2021-10-01</span>_extended.gif
<span class="hljs-strong">2021-10-01</span>_extended_domain.png
<span class="hljs-strong">2021-10-01</span>_extended_lsta_imerg.png
<span class="hljs-strong">2021-10-02</span>_extended_domain.png
<span class="hljs-strong">2021-10-02</span>_extended_lsta_imerg.png
</code></pre>

</span>

</span>

</div>


#--

### File naming conventions

- Break up file names using standard separators

```
 S_NWC_CRR_MSG4_global-VISIR_20210219T100000Z.nc

|-|---|---|----|------------|----------------|
        |    |     |                 |
     product |   domain       date/timestamp
             |
         satellite
```

<ul>
<li class="fragment fade-in">Easier to understand</li>
<li class="fragment fade-in">Easier to automate processing</li>
</ul>


#--

### File naming conventions

- Avoid making multiple versions of files &ndash; use <a href="#/versioncontrol">version control</a> instead!

<span class="fragment fade-in">

<pre><code data-trim data-noescape>
my_script.R
my_script<span class="hljs-strong">_second_version</span>.R
my_script<span class="hljs-strong">_FINAL</span>.R
my_script<span class="hljs-strong">_FINAL_latest</span>.R
</code></pre>
</span>

<span class="fragment fade-in">
- More about version control later...
</span>

#--

### Directory structure

- An organised and self-contained directory structure will help you to
    - Encapsulate work on a project
    - Clarify dependencies between different components
    - Find your way around when you come back to earlier work

#--

### Directory structure

- Use a standard directory structure e.g. different folders for data, scripts etc

```
.
|-- chapter1/
    |
    |-- code/
    |-- data/
    |-- figures/
    |-- paper/

```

<span class="fragment fade-in">

- Project templates can be useful for setting up standardised directory structure

</span>

#--

### Directory structure

- https://github.com/bvreede/good-enough-project

```
.
|-- CITATION.md
|-- config
|-- data
|   |-- processed
|   |-- raw
|   |-- temp
|-- docs
|   |-- manuscript
|-- |-- reports
|-- LICENSE.md
|-- README.md
|-- requirements.txt
|-- results
|-- |-- figures
|-- |-- output
|-- src
```

#--

### Directory structure

- Use relative paths to refer to files within the project directory
  - Easier to move project directory to different location

#--

#### Example: Relative paths

```
|
|-- code/
|   |-- plot_aq.R
|
|-- data/
|   |-- aq_devonshire_green.csv
|
|-- figures/
|-- paper/
```

##### `code/plot_aq.R`


```r
mydata <- read.csv("../data/aq_devonshire_green.csv")

# data manipulation and plotting code...

ggsave("../figures/fig1_aq_devonshire_green.png")

```

#--

### Metadata

- Data that describes other data
- Adds value to data
  - Enables (re)use and interpretation
  - Promotes data discovery and long term viability

#--

### Types of metadata

- Descriptive
  - When and where data collected
  - Who collected the data
  - Environmental conditions
  - Units, precision etc
  - Methodology
  - Research questions

#--

### Types of metadata

<!-- - Structural -->
<!--  - Describes relationships between data components -->
<!--  - Multi-channel satellite imagery? -->
<!--  - Genome sequence data - chromosome number -->


- Administrative
  - Creator
  - Funding info
  - License info

#--

### Types of metadata

- Structural
- Provenance
- Use

#--

### Metadata standards

- Using a standardised metadata format makes it easier to find and reuse data
- Many different, discipline specific [metadata standards](http://rd-alliance.github.io/metadata-directory/standards/)
- XML schema often used to define structure
- Software tools for creating and reading metadata


#--

#### Example: CF (Climate and Forecast) Metadata Conventions

- Suitable for model-generated climate forecast data and observational datasets
- Information included:
  - variable description, units, and prior processing
  - spatial and temporal coordinates
  - creation and provenance of data
- http://cfconventions.org/

#--

### File formats

<ul>
<li class="fragment fade-in">Data comes in many different shapes and sizes</li>
<li class="fragment fade-in">Choose an appropriate format for your data
<ul>
<li>Flat vs structured/hierarchical</li>
<li>Proprietary vs open formats</li>
</ul>
</li>
<li class="fragment fade-in">Consider accessibility/portability
  <ul>
  <li>Will you need to use particular software to access your data?</li>
  </ul>
</li>
</ul>

#--

## Maintaining data integrity<br/>

<ul>
<li class="fragment fade-in">Treat your raw data as something that shouldn't be changed</li>
<li class="fragment fade-in">Record any processing steps required and store processed data separately</li>
<li class="fragment fade-in">Use scripts for processing data to aid reproducibility</li>
</ul>

#--
## Storage and backup


#--
### Storage space considerations

<ul>
<li class="fragment fade-in">
How much space do you need?
<ul>
<li>What is the size of a typical unit of data?<br/>
e.g. daily air quality readings, single model run</li>
<li>How many data units will you create?</li>
</ul>
</li>
<li class="fragment fade-in">
Who needs access to the data?
<ul>
<li>File permissions and access requirements</li>
</ul>
</li>
<li class="fragment fade-in">
Does the storage space get backed up?
</li>
<li class="fragment fade-in">
Can you access stored data to carry out your analysis?
</li>
</ul>

#--
### Backing up your data and scripts

- On-site and off-site backup
- Removable storage
- Frequency of backup
- Ensuring sufficient capacity
- Transfer speed
