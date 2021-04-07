<img src="img/data_lifecycle_create.png" width="30%" />

#--

## Data creation and acquisition

#--

## Organising and describing your data<br/>

- Make it easy to understand 


#--

### File naming conventions

- Use file names to reflect logical order of work

```
01-import_data.R
02-first_analysis.R
03-second_analysis.R
```

--

- Use ISO 8601 format for dates: `YYYY-MM-DD` or `YYYYMMDD`

```
20200827/dewpoint_2m/GFSanalysis_EA_2020082706_DPTMP2_SNGL.png
```

--

- Break up file names using standard separators

  - Easier to understand
  - Easier to automate processing

```
 S_NWC_CRR_MSG4_global-VISIR_20210219T100000Z.nc

|-|---|---|----|------------|----------------|
        |    |    |                  |
     product |  domain        date/timestamp
             |
         satellite
```

--

- Avoid making multiple versions of files — use version control instead!

```
my_script.R
my_script_second_version.R
my_script_FINAL.R
my_script_FINAL2.R
```

#--

### Metadata


#--

### File formats

#--

## Maintaining data integrity<br/>


#--
## Storage and backup


#--
### Storage space considerations

* How much space do you need? Estimating space.  
* Who needs access to data?  
* Does storage space get backed up?  

#--
### Backing up your data and scripts


#==

