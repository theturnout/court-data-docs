JSON-LD
=======

Schema.org supports a number of formats, including inline RDFa. While RDFa markup that is integrated directly with HTML provides the most convenient way to keep information provided on a website in parity with that provided to search engines, it has a high initial cost of setup that may be prohibitive to web developers looking to incorporate the standard into existing HTML code. For that reason, JSON-LD was chosen as the data format supported by the Court Data Standard and its tooling. While there is a higher maintenance cost once the standard is implemented as information provided by a website must be manually kept in parity with the accompanying JSON-LD file, it has a very low cost of adoption and the effort required to keep the information in both documents in parity is still low.

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

General Standards
-----------------

JSON-LD data, whether stored in a separate file or included inline with HTML, must be surrounded by braces. Additionally, each indented level of data should also be surrounded by braces. Data is stored in property-value pairs in the following format: "property": "value". Note the quotation marks surrounding each string. Multiple properties in the same level are separated by a comma and a line break.

.. code-block:: json

    {
        "top-level property": {
            "sub-property": "some value",
            "another sub-property": "another value"
        }
    } 

Nested Properties
-----------------

Consider a courthouse with multiple courts. Nesting properties, such as operating hours, makes it clearer with which court the hours are associated and avoids confusion that may arise from identical properties being included in the same level.

A conceptual example of best practice for the organization of information follows.

.. code-block:: text

    Court A
        Operating Hours
    Court B
        Operating Hours

File Structure and Syntax
-------------------------

The top level of data should begin with an indication of the source of the schema the file follows. A URL to the schema is typically used as the value rather than its name: :code:`"@context": "https://schema.org"`. Each level should also indicate the type of Thing that is being described if it is different than the type of the level above it: :code:`"@type": "ATypeOfThing"`. Information about Things, Types, properties, and other terms can be :link:"`found in the documentation provided on Schema.org <https://schema.org/docs/styleguide.html>`_.

Example Model
-------------

The following model demonstrates how these rules come together to create a JSON-LD file. Note that it does not represent all of the data that may be included in a file. The information used is taken from https://www.illinoiscourts.gov/courts-directory/66/Adams-County-Courthouse/court/ which can be referenced to compare the presentation of data on a webpage and in a JSON-LD file.

1. To start, provide the source of the schema being applied at the top of the file. 

.. code-block:: json

    {
        "@context": "https://schema.org"
    }

2. Next, indicate the property used to record a court's location. In this case, it is :code:`address`. Referencing the property :doc:`Properties </dictionary/properties>` section for :code:`address`, we see that the value for the :code:`address` property is a type: :code:`PostalAddress`. Property values that are types (not all are) are recorded as embedded objects. For now, we'll leave the object empty. 

.. code-block:: json

    {
        "@context": "https://schema.org",
        "address": { }
    }

3. Here we have to identify the type and :code:`@context` where the type's definition can be found. The type is recorded with the :code:`@type` property and is a direct link to the type's definition. This is the "Linked" component of "Linked Data".

.. code-block:: json

    {
        "@context": "https://schema.org",
        "address": { 
            "@context": "https://schema.org",
            "@type": "https://schema.org/PostalAddress"    
        }
    }

4. Now we can record the properties associated with the address of the thing being described. Reviewing the :doc:`Structured Type </dictionary/structured_types>` documentation for :code:`PostalAddress` suggests that there are four properties that can be used to express a US address: :code:`streetAddress`, :code:`addressLocality`, :code:`addressRegion`, and :code:`postalCode`. We'll add these to our file to complete the :code:`address` record.

.. code-block:: json

    {
        "@context": "https://schema.org",
        "address": { 
            "@context": "https://schema.org",
            "@type": "https://schema.org/PostalAddress",
            "streetAddress": "521 Vermont Street",
            "addressLocality": "Quincy",
            "addressRegion": "IL",
            "postalCode": "62301"
        }
    }