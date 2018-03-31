# Download PubMed Central articles with meta-data

The [PMC Open Access Subset](https://www.ncbi.nlm.nih.gov/pmc/tools/openftlist/) is a part of the total collection of articles in PMC. The articles in the OA Subset are made available under a Creative Commons or similar license that generally allows more liberal redistribution and reuse than a traditional copyrighted work. PubMed Central maintains a database of all open access articles, for each of which it holds: an XML with all relevant meta-data, all images, its PDF version and all of its supplementary files, if any. These data can be downloaded using two services: the [PMC OAI service](https://www.ncbi.nlm.nih.gov/pmc/tools/oai/) or the [PMC FTP service](https://www.ncbi.nlm.nih.gov/pmc/tools/ftp/). The PMC OAI service provides access to metadata of all items in the PubMed Central (PMC) archive, as well as to the full text of a subset of these items.

## To download all XML and TXT files

These files contain the extracted abstract, full text, tables, references and meta-data (e.g. date of publication, type of publication, etc.) for each article. They are available in either .xml or .txt format. 

To download manually, go to ftp://ftp.ncbi.nlm.nih.gov/pub/pmc/oa_bulk/ and download your collections of interest. Then, run the following in your terminal to decompress the files you downloaded into a folder called "data".

```
mkdir data
tar -xvf non_comm_use.0-9A-B.txt.tar.gz -C data
```

To download automatically in .xml, run the following shell script provided on this repository in your terminal within the directory (i.e. folder) you'd like to save these data.

```
sh pmc_download.sh
```

## To download one article package at a time

1. Visit the [Open Access Subset](https://www.ncbi.nlm.nih.gov/pmc/tools/openftlist/) website of PubMed Central.

2. Download a CSV file with a reference to every article on PMC and their respective file names using the PMC FTP service [here](ftp://ftp.ncbi.nlm.nih.gov/pub/pmc/oa_file_list.csv).

3. Example website to download file **oa_package/08/e0/PMC13900.tar.gz**:

    ftp://ftp.ncbi.nlm.nih.gov/pub/pmc/oa_package/08/e0/PMC13900.tar.gz
  
## To download one article .xml at a time

To download the .xml file as above for article with PMC 156895 use:

https://www.ncbi.nlm.nih.gov/pmc/oai/oai.cgi?verb=GetRecord&identifier=oai:pubmedcentral.nih.gov:156895&metadataPrefix=pmc

For more examples on what can be done using the PMC OAI service, visit its [website](https://www.ncbi.nlm.nih.gov/pmc/tools/oai/).
