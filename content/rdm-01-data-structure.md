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

- Use your lab and field notes to record information that will be required for correct interpretation of data
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

- When you've entered and checked your data, protect the file from further changes

#--
<!-- .slide: id="tidydata" -->
### Tidy data principles

- Differentiate between:
  - Variables (things that you've measured for each unit)
  - Observations (all measurements for a single unit)

- Variables are stored in **columns**, observations are stored in **rows**

<span class="footnote"><a href="https://www.jstatsoft.org/article/view/v059i10">Tidy Data, Wickham, 2014, Journal of Statistical Software</a></span>

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

<span style="font-size:smaller">Hourly measured PM2.5 particulate matter, Sheffield Devonshire Green</span>

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

<span style="font-size:smaller">Hourly measured PM2.5 particulate matter, Sheffield Devonshire Green</span>

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

### Data from an external service

- What is the interface for accessing data?
  - Order form on website
  - Remote access e.g. ftp

- Do you know how long it will take to get the data that you need?
- Time to process order request
- Data size limitations
  - Download times
  - Accessing archived data may have greater latency

- Permissions

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

- Use file names to reflect logical order of work

<pre><code data-trim data-noescape>
<span class="hljs-strong">01</span>-import_data.R
<span class="hljs-strong">02</span>-first_analysis.R
<span class="hljs-strong">03</span>-second_analysis.R
</code>
</pre>

#--

### File naming conventions

<div class="left">

- Use ISO 8601 format for dates: `YYYY-MM-DD` or `YYYYMMDD`

<span class="fragment fade-in">

- Ensures correct order when listing files

<span class="fragment fade-in-then-out">
<pre><code data-trim data-noescape>
GFSanalysis_EA_<span class="hljs-strong">21042021</span>_06_DPTMP2_SNGL.png
GFSanalysis_EA_<span class="hljs-strong">27082020</span>_06_DPTMP2_SNGL.png
</code></pre>
</span>

<span class="fragment fade-up">
<pre><code data-trim data-noescape>
GFSanalysis_EA_<span class="hljs-strong">20200827</span>_06_DPTMP2_SNGL.png
GFSanalysis_EA_<span class="hljs-strong">20210421</span>_06_DPTMP2_SNGL.png
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

- Avoid making multiple versions of files &ndash; use version control instead!

```
my_script.R
my_script_second_version.R
my_script_FINAL.R
my_script_FINAL2.R
```

#--

### Directory structure

- encapsulate work on a project
- use relative paths - easier to move project directory to diff location
- store files according to a standard structure e.g. different folders for data, scripts etc



#--

### Metadata

- Data that provides information about other data
- Add value to data
- Allow use and interpretation


What sort of things might be recorded?
[check RDMe materials]

- when and where data collected
- environmental conditions
- units, precision etc
- methodology
- research questions
- creator
- license info

Metadata standards



#--

### File formats

- choose correct format for data
- accessibility/portability



#--

## Maintaining data integrity<br/>

- Treat your raw data as something that shouldn't be changed
- Record any pre-processing steps required and store outputs separately
- Use scripts for pre-processing to aid reproducibility


#--
## Storage and backup


#--
### Storage space considerations

* How much space do you need? Estimating space.  
* Who needs access to data?  
* Does storage space get backed up?  

#--
### Backing up your data and scripts

- Removable storage
- 

#==

