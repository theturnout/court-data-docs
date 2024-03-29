The Court Data Pipeline
=======================

To support court administrators, researchers, or anyone else interested in aggregating publically available information about courthouses, tools to automate the collection, validation, and storage of files created using the Court Data Standard have been developed. At a high level, JSON-LD information hosted by individual courthouses can be scraped from websites in bulk, validated for compliance with the standard, and stored in an RDF datastore. The datastore can be built using a variety of database dialects and is intended to be as agnostic to the end user's environment as possible.

The Court Data Pipeline is written in Python using open source tools and is open source itself. Anyone with an interest in exploring or implementing the Court Data Standard may use it.

Github Repo: https://github.com/theturnout/court-data-pipeline

Requirements
------------
* Python >= 3.10
* pipenv >= 2022.10.11

Description
-----------

The Court Data Pipeline is designed to scrape websites provided as a list of URLs in a CSV file. It looks for JSON-LD files either linked from or embedded in HTML source code and downloads or scrapes and parses the data to save it locally. The files are then validated against a `SHACL schema <https://www.w3.org/TR/shacl/>`, with property values checked against constraints defined by remote sources identified in the JSON-lD file. After passing validation, the JSON-LD data is then loaded into a database. The database can be queried using `SPARQL <https://www.w3.org/TR/sparql11-query/>` as the query language.

Components
~~~~~~~~~~

The pipeline is broken into three main functions: web scraping, validation, and storage. Source code for the scraper can be found in :code:`classes/json_scraper.py`, for the validator in :code:`classes/validator.py`, and for the DB importer in :code:`components/data_importer.py`.

Web Scraping
************

The :code:`scrapy` library is used as the basis for web scraping functions. The script ingests a CSV file of URLs provided as an argument when calling the main :code:`app.py` script from the CLI. The provided websites are crawled and, where JSON-LD data is found, it is parsed and saved in the :code:`data/json/scraped` directory.

Validation
**********

Constraints for JSON-LD files are defined in a SHACL file, which identifies permitted values for types and properties on https://schema.org and as well as developed for the Standard. The SHACL file and the Court Data Standard definitions created for this project can be found in the :code:`data/defs` directory. The validation itself is performed by :code:`pyshacl`. Files that pass validation are then passed to the :code:`data_importer` script.

Storage
*******

Data passed from the :code:`validator` is parsed and transformed from RDF triples to flat data that can be stored in SQL datastores. Data in these stores is not very human-readable but can be reassembled using SPARQL queries. The :code:`queries` directory contains examples of SPARQL queries and the `run_query.py` script that can be run to extract data stored by the pipeline. See the documentation in the tool's GitHub repo, linked above, for more information about executing SQARQL queries on the Court Data Standard example data.