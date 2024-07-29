<!-- .slide: id="metadata" -->
## Metadata and standards

#--

### What is metadata?

<ul>
  <li class="fragment fade-in">
    Metadata is data that describes other data</li>
  <li class="fragment fade-in">
    Attaching metadata to a dataset allows others to find and use the data effectively
  </li>
  <li class="fragment fade-in">
    Metadata can be stored separately or embedded within a data file
</ul>

#--

### Benefits of metadata

<ul>
  <li class="fragment fade-in">
    Attaching metadata to a dataset adds value by
    <ul>
      <li class="fragment fade-in">
        Promoting (re)use and interpretation
      </li>
      <li class="fragment fade-in">
        Enabling data discovery through metadata-based search within data repositories
      </li>
    </ul>
  </li>
  <li class="fragment fade-in">
    Metadata enhances the long-term viability of data
  </li>
</ul>

#--

### Types of metadata

<ul>
  <li class="fragment fade-in">
    Descriptive (when, where and by whom were the data collected, research questions, methodology, units/precision)</li>
    <li class="fragment fade-in">
      Administrative (license, funders, version)</li>
  <li class="fragment fade-in">
    Structural (archive/file structure, number of files)</li>
  <li class="fragment fade-in">
    Provenance (source of raw data, processing steps)
  </li>
</ul>

#--

### Using metadata to describe research data

<ul>
  <li class="fragment fade-in">Data comes in many different shapes and sizes
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

### Hierarchical data formats

<ul>
  <li class="fragment fade-in">
    Hierarchical data uses internal structure to store metadata
  </li>
  <li class="fragment fade-in">
    This allows a dataset to be self-describing and promotes portability and scalability
  </li>
  <li class="fragment fade-in">
    NetCDF is a commonly used hierarchical data format
  </li>
</ul>

<!-- <p class="footnote"><a href="https://www.unidata.ucar.edu/software/netcdf/index.html">https://www.unidata.ucar.edu/software/netcdf/index.html</a></p> -->

#--

### Metadata standards

<ul>
  <li class="fragment fade-in">
    Using a standardised metadata format makes it easier to find and reuse data
  </li>
  <li class="fragment fade-in">Many different, discipline specific metadata standards (see e.g. <a href="https://rdamsc.bath.ac.uk/">RDA Metadata Standards Catalog</a>, <a href="https://fairsharing.org/standards/">FAIRsharing.org</a>)</li>
  <li class="fragment fade-in">XML schema often used to define structure</li>
  <li class="fragment fade-in">Software tools for creating and reading metadata</li>
</ul>


#--

#### Example: [Climate and Forecast Metadata Conventions](http://cfconventions.org/)

<ul>
  <li class="fragment fade-in">
    Suitable for model-generated climate forecast data and observational datasets</li>
  <li class="fragment fade-in">
    Information included:
    <ul>
      <li class="fragment fade-in">
        variable description, units, and prior processing
      </li>
      <li class="fragment fade-in">
        spatial and temporal coordinates
      </li>
      <li class="fragment fade-in">
        creation and provenance of data
      </li>
    </ul>
  </li>
  <li class="fragment fade-in">Includes a standard name table for identifying physical quantities</li>
</ul>
