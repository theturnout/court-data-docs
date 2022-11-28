Data Format
===========

Schema.org supports a number of formats, including inline RDFa. While markup that is integrated directly with HTML provides the most convenient way to keep information provided on a website in parity with that provided to search engines, it has a high initial cost of setup that may be prohibitive to web developers looking to incorporate the standard into existing HTML code. For that reason, JSON-LD was chosen as the data format supported by the Court Data Standard and its tooling. While there is a higher maintenance cost once the standard is implemented as information provided by a website must be manually kept in parity with the accompanying JSON-LD file, it has a very low cost of adoption and the effort required to keep the information in both documents in parity is still low.

JSON-LD
-------

JSON-LD is lightweight data format that is preferred by Google for the creation of Google Rich Text and can be used by the search engine to automatically generate the information boxes that appear to the right of search results pages when enough information about a subject is available. In cases where search results are ambiguous due to court names or overly-broad user search terms and an information box is not generated, the format can still make information more visible by increasing the likelihood that a relevant page is returned in search results.

The "LD" in JSON-LD stands for linked data. The format allows information contained within files to be linked to external data sources. This means that schema and constraint information can be provided by external third-party sources and does not need to be included in JSON-LD files themselves. The external data is referenced at the time of validation, so it will always be consistent with the most current version of the vocabulary being used.

More information about the JSON-LD format is available at https://json-ld.org/.

JSON-LD Standards and Practices
-------------------------------

JSON-LD organizes data similarly to JSON. Familiarity with the latter is sufficient for understanding JSON-LD. For users unfamiliar with JSON, an example record indicating a courthouse's address will be created step-by-step with explanations provided for each implemented practice or rule.

When building an HTML document, it is necessary to add the following line to the HTML header to indicate that the JSON-LD file should be imported and where it is located.

.. code-block:: html

    <link href="<PATH_TO_JSON-LD_FILE>" rel="alternate" type="application/ld+json" />
    
Alternatively, the JSON-LD data may be embedded inline by inserting it between the script tags in the following line. This is not recommended for readability reasons but can be done if the above method does not work. The script tags should be added to the end of the HTML document, just inside the closing :code:`<body>` tags.

.. code-block:: html

    <script type="application/ld+json">
        <DATA>
    </script>

[...]