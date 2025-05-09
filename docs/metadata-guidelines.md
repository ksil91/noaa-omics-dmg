Metadata Guidelines
======

Metadata are contextual data about your experimental data. Metadata are the who, what, when, where, and why of these data. Metadata put these data into context. For 'omics studies, metadata include information about the sample: when it was collected, where it was collected from, what kind of sample it is, and what were the properties of the environment or experimental condition from which the sample was taken. Information about sample processing is also metadata: methods used to extract and purify molecules (e.g., DNA) from the sample, type of DNA sequencing or other ’omics analyses done, and where the raw experimental data are located.

For an 'omics study, metadata exist at multiple stages along the path from samples to analysis. For example, contextual information about when and where the sample was collected could include descriptors like date, time, and geospatial coordinates. Processing the sample in the lab for analysis requires different protocols and instrumentation. Once these data become electronic and are analyzed, the results should be accompanied by the versioned software used.

Metadata can also refer to information about the study itself and where the data can be found (both online and offline) in order for potential users to discover, access, evaluate, and use the data. Metadata of this type is required by the [NOAA Data Management Handbook](https://sites.google.com/noaa.gov/noaa-data/handbook) and should be hosted by NCEI.  

## Categories of metadata

### Sample metadata

Information about the primary sample: when it was collected (e.g., date and time), where it was collected from (e.g., latitude, longitude, elevation/depth, site name, country, etc.), what kind of sample it was (e.g., soil, seawater, feces), and the properties of the environment during collection (e.g., temperature, salinity, pH) or experimental condition (e.g., experimental or control, disease state) from which the sample was taken. Sample metadata are not dependent on how the sample was processed; that is called preparation metadata (see next item).

*Most of this would not be considered metadata in the strict (non-omics) sense. It is data, but it is used as contextual data for the omics data.* 

### Experimental metadata

* **Preparation metadata**: how samples were extracted, how samples were sequenced; this is specified by the MIxS 
* **Data processing/analysis metadata**: data about processing from raw sequences to desired outputs (e.g., sequence properties, software versions, processing parameters    
* **Feature metadata**: ID number, assembled sequences, assigned taxonomy/function/genome location 

<!-- ### Project metadata  -->


## Recording metadata

Planning how and what metadata is recorded in a standardized way from the start of every project will go a long way towards saving time when submitting your data to data repositories, as well as improving overall research reproducibility. Using standardized [templates]((https://noaa-omics-dmg.readthedocs.io/en/latest/study-data-templates.html) early in the data collection process can help tremendously. Typically, each individual sample is recorded as a row and metadata attributes for each sample are recorded in columns. The specific metadata attributes will vary depending on your 'omics method, but generally the sample metadata should contain the minimum, yet comprehensive information about the physical and chemical conditions of the sample, from collection through sequencing. A (non-comprehensive) list could include sampling environment, molecular lab procedure names, sequencing platform and model (required by NCBI SRA), and data processing steps, and external identifications from additional processing steps, e.g. sample IDs from a sequencing organization. 

Metadata should be collated from primary sources (e.g., paper notes, emails, external collaborators, lab notebooks) and associated with sample IDs as soon as possible after it is generated. Primary sources of metadata should be backed up in case they are needed as a reference later. During this stage, the metadata should be evaluated for potential errors (e.g., incorrect GPS coordinates, missing data) and followed up on with the original data collector.

## Metadata formats and custom fields

While templates from NCBI provide some information of formatting and support the minimum metadata required for submission, we highly recommend providing additional metadata following relevant standards such as [Darwin Core](https://dwc.tdwg.org/terms/) for biodiversity observations and [FAIRe](https://fair-edna.github.io/index.html) for eDNA data. Check out the [Study Data Templates](https://noaa-omics-dmg.readthedocs.io/en/latest/study-data-templates.html) section for templates to help use these terms. 

## Refining metadata to a standard

Standardizing the format of your metadata can both facilitate sharing of your results with others and improve identification of errors within your own metadata. Having a method-specific template Google Sheet or Excel file for metadata that you use across all similar studies can be very helpful. This template should include a second sheet or file with a "data dictionary" defining the desired attribute columns and formats. Refining your metadata to a standard has benefits for internal use, publication, and repository submission. Refined metadata should have the following characteristics:

1. Standardized: The data in each column should be written in a consistent manner, i.e. in the same format. 
2. Well-defined attributes: The names of the metadata parameters of each sample should be obvious in definition, with units included if applicable.
3. Collected metadata should be comprehensive, but not with extraneous or unnecessary attributes.

A general workflow for transforming and refining metadata:

1. Fill in missing metadata: consult cruise/ship notes and other potential sources of unconsolidated information about the samples. For missing data that cannot be filled in, we recommend following the [INSDC standardized missing value reporting language](https://ena-docs.readthedocs.io/en/latest/submit/samples/missing-values.html).
2. Identify the columns that are present and compare that with those in the data dictionary, given that those are the minimum amount of information that we hope to submit with the dataset that we make publicly available.
3. Standardize the data to that of the column headers’ standards. 
4. Optional: input columns to relational database
5. Publish data to NCEI and other potential funding specific sites

## Submitting metadata and environmental data to repositories

NOAA ’Omics projects should make their metadata and non-’omics data (non-“big data”) publicly accessible to the appropriate repositories (also see [Table 1](https://noaa-omics-dmg.readthedocs.io/en/latest/omics-data-guidelines.html#table-1-data-repositories)). Please note that, although NOAA's Coral Reef Information System ([CoRIS](https://www.coris.noaa.gov/data/supportingdocs.html)) is the preferred venue for archiving NOAA-funded coral reef data, all CoRIS submissions are handled by NCEI.

| Project type          | Metadata repositories     | 
| --------------------- | ------------------------- | 
| Environmental survey  | [OBIS/GBIF](https://noaa-omics-dmg.readthedocs.io/en/latest/metadata-guidelines.html#submitting-to-biodiversity-repositories-obisgbif) or directly to [NCEI](https://www.ncei.noaa.gov/archive); [NCBI](https://www.ncbi.nlm.nih.gov/sra/docs/submit/#accepted-data)               |
| Mesocosm experiment   | [NCEI](https://www.ncei.noaa.gov/archive) & [NCBI](https://www.ncbi.nlm.nih.gov/sra/docs/submit/#accepted-data)                 |
| Laboratory experiment | [NCBI](https://www.ncbi.nlm.nih.gov/sra/docs/submit/#accepted-data)                        |
| Genome/reference sequencing | [NCBI](https://www.ncbi.nlm.nih.gov/sra/docs/submit/#accepted-data)                  |
| Non-DNA/RNA data (e.g.: metabolomics, proteomics) | Specialized repository and/or [NCEI](https://www.ncei.noaa.gov/archive) (if environmental), [NCBI](https://www.ncbi.nlm.nih.gov/sra/docs/submit/#accepted-data)  |
| Coral reef data | [CoRIS](https://www.coris.noaa.gov/data/supportingdocs.html) (via [NCEI](https://www.ncei.noaa.gov/archive)), with cross-linking to relevant data repository |

<!--
Can we submit metadata to BioSample without sequence data?
\!-->

### Use GCMD keywords in project metadata  

Whenever you submit metadata about a project to a repository, if there is a field for keywords we recommend using a controlled vocabulary such as the [Omics terms in the NASA Global Change Master Directory (GCMD)](https://gcmd.earthdata.nasa.gov/KeywordViewer/scheme/Earth%20Science/8eb84f36-f355-458b-889f-b37cfa120654?gtm_keyword=OMICS&gtm_scheme=Earth%20Science). GCMD keywords are a hierarchical set of controlled Earth Science vocabularies that help ensure Earth science data, services, and variables are described in a consistent and comprehensive manner and allow for the precise searching of metadata and subsequent retrieval of data, services, and variables. 

### NCEI

Send metadata and environmental data to the [National Centers for Environmental Information (NCEI)](https://www.ncei.noaa.gov/), generally excluding ’omics data, as these large datasets should be stored in the relevant [long-term data repository](https://noaa-omics-dmg.readthedocs.io/en/latest/omics-data-guidelines.html#table-1-data-repositories) and linked from NCEI to those records with persistent identifiers. Although NCEI can curate ’omics datasets smaller than 20 GB (i.e., most proteomic and metabolomic datasets), it does not permit the critically important interactive querying feature that is integral to all ’omics-tailored data repositories and so should not be the lone repository for ’omics data. We highly recommend submitting metabarcoding ASV tables to OBIS/GBIF (see next section).

### Submitting to biodiversity repositories (OBIS/GBIF)

[GBIF](https://www.gbif.org/) and [OBIS](https://obis.org/) are global repositories of biodiversity data, and are actively interested in expanding access to eDNA observations. OBIS has the benefit of archiving data to NCEI for you. 

NOAA Omics has developed a Python workflow for preparing data for submission to OBIS/GBIF, called [edna2obis](https://github.com/aomlomics/edna2obis). This workflow requires some familiarity with Jupyter Notebooks and Python.

GBIF also has a non-coding [prototype GUI tool](https://edna-tool.gbif-uat.org/) to prepare eDNA data for GBIF/OBIS.  

For general guidance on preparing data for OBIS/GBIF, check out the guide entitled "[Publishing DNA-derived data through biodiversity data platforms](https://docs.gbif.org/publishing-dna-derived-data/en/)."

OBIS also has a free self-paced [course](https://oceanexpert.org/event/3983) for preparing and submitting data, including a module on DNA-derived data.

### Domain-specific databases 

* Ocean acidification (OA) data generated through the Ocean Acidification Program (OAP) should be submitted to a special section of NCEI, the [Ocean Acidification Data Stewardship (OADS) Project](http://www.nodc.noaa.gov/oceanacidification).  
* Coral and coral reef data should be sent to NCEI, where it will then be posted on NCEI and referenced/cross-listed by NOAA’s [Coral Reef Information System (CoRIS)](https://www.coris.noaa.gov/).
* [Earth Science Information Partners (ESIP)](https://www.esipfed.org/esip-endorsed) Biological Data Standards.  
* [International Organization for Standardization (ISO)](https://www.iso.org/) standards with guidance from NOAA’s [National Centers for Environmental Information (NCEI)](https://www.ncei.noaa.gov/).

### Metadata standards

Environmental metadata should be formatted according to one or more of the following standards:  
* [ISO I9115-2](https://www.ncei.noaa.gov/sites/default/files/2020-04/ISO%2019115-2%20Workbook_Part%20II%20Extentions%20for%20imagery%20and%20Gridded%20Data.pdf)
* Water samples (NOAA Omics standard): [Study Data template - Water](https://docs.google.com/spreadsheets/d/1YBXFU9PuMqm7IT1tp0LTxQ1v2j0tlCWFnhSpy-EBwPw/edit?usp=sharing)
* General ’omics projects: [Genomics Standards Consortium (GSC) Minimum Information about any (x) Sequence (MIxS)](https://github.com/GenomicsStandardsConsortium/mixs/wiki).
* OAP-funded projects: [Ocean Acidification Data Stewardship (OADS)](https://www.ncei.noaa.gov/products/ocean-carbon-acidification-data-system) metadata guidelines.
* Additional guidance from [ENA](https://ena-docs.readthedocs.io/) (European Nucleotide Archive), including [The ENA Metadata Model — ENA Training Modules 1 documentation](https://ena-docs.readthedocs.io/en/latest/submit/general-guide/metadata.html) and [Reporting Missing Values — ENA Training Modules 1 documentation](https://ena-docs.readthedocs.io/en/latest/submit/samples/missing-values.html). 

### Timing of submission

The suggested deadline for data to be published and accessible in NCEI is one year after the end date of the project for NOAA intramural PIs, two years after the end date of the project for extramural PIs, or before a paper is published using these data (whichever is sooner). This schedule is based on the [OAP Data Management Agreement](https://www.ncei.noaa.gov/products/ocean-carbon-acidification-data-system).  

**Point of contact for submissions**: The PI is responsible for working with NCEI to publish the data in a timely manner.  

## Useful links

Metadata guides  
  + [National Microbiome Data Collaborative (NMDC)](https://microbiomedata.org/introduction-to-metadata-and-ontologies/) -- covers additional metadata
  + [Earth Microbiome Project (EMP)](https://earthmicrobiome.org/protocols-and-standards/metadata-guide/)

Metadata standards  
  + [GSC defined terms](https://www.gensc.org/pages/standards/all-terms.html)
  + [Biosample Attributes](https://www.ncbi.nlm.nih.gov/biosample/docs/attributes/)
  + [BeBOP-OBON Protocol Collection Template](https://github.com/BeBOP-OBON/0_protocol_collection_template)
  + [BeBOP-OBON Minimum Information about an Omics Protocol](https://github.com/BeBOP-OBON/miop)
  + [GBWG - Sustainable DarwinCore MIxS Interoperability - TDWG](https://www.tdwg.org/community/gbwg/mixs/)
  + [GenBank templates](https://submit.ncbi.nlm.nih.gov/templates/)
  + [NIH tool to format all types of metadata](https://metagenote.niaid.nih.gov/)
