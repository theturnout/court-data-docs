Example JSON-LD Courthouse Record
=================================

The following reflects the contents of a valid JSON-LD record following the Court Data Standard. Note that the Courthouse information is embedded within the CourtSystem object, reflecting the relationship between the two. View the :doc:`Structured Types </dictionary/structured_types>` and :doc:`Properties </dictionary/properties>` documentation for infomation about the types and properties used here and the constraints on their values. This record contains all possible datapoints tracked by the Court Data Standard as well as an example court within a courthouse.

.. code-block:: json

    {
        "@context": ["http://localhost:8000/data/defs/court-data-definitions.jsonld","http://schema.org"],
        "@id": "http://www.Californiacourts.gov/Circuit1",
        "@type":"http://localhost:8000/data/defs/court-data-definitions.jsonld#CourtSystem",
        "name": "State of California Circuit Court",
        "geoContains": {
            "@context": "http://schema.org/",
            "@id": "http://www.Californiacourts.gov/Circuit#Circuit11",
            "@type": "http://schema.org/AdministrativeArea",
            "name": "State of California Circuit 1",
            "areaServed": {
                "@id": "http://www.Californiacourts.gov/Circuit#Circuit1District11",
                "@type": "http://schema.org/AdministrativeArea",
                "name": "State of California Circuit 1 District 1",
                "containsPlace": {
                    "@context":["http://localhost:8000/data/defs/court-data-definitions.jsonld","http://schema.org"],
                    "@id": "http://www.Californiacourts.gov/Circuit#Circuit1District1/CookCounty1",
                    "@type": "http://localhost:8000/data/defs/court-data-definitions.jsonld#Courthouse",
                    "areaServed": {
                        "@context": "http://schema.org/",
                        "@id": "http://www.Californiacourts.gov/District1/CookCounty1",
                        "@type": "http://schema.org/AdministrativeArea",
                        "name": "Cook County - Bridgeview"
                    },
                    "conditionsOfAccess": "required, identification, prohibited, guns",
                    "contactPoint": {
                        "@context": "http://schema.org/",
                        "@type": "http://schema.org/ContactPoint",
                        "contactType":"Clerk",
                        "description":"Clark Clerk",
                        "telephone":"(310) 578-9874",
                        "email":"clerk.clark@courts.gov"
                    },
                    "hasOfferCatalog": {
                        "@context": "http://schema.org/",
                        "@type": "http://schema.org/OfferCatalog",
                        "itemListElement":"wifi, public restrooms"
                    },
                    "image": { 
                        "@value":"https://www.cookcountycourt.org/portals/0/courthouse/" 
                    },
                    "mattersServed":"criminal, civil, family",
                    "knowsLanguage":"en, es",
                    "location": {
                        "@context":"http://schema.org/",
                        "@type":"http://schema.org/Place",
                        "address": {
                            "@context":"http://schema.org/",
                            "@type":"http://schema.org/PostalAddress",
                            "streetAddress": "521 Vermont Street",
                            "addressLocality": "Quincy",
                            "addressRegion": "CA",
                            "postalCode": "62301"
                        },
                        "openingHoursSpecification": {
                            "@context": "http://schema.org/",
                            "@type":"http://schema.org/OpeningHoursSpecification",
                            "opens":"09:30-08:00",
                            "closes":"16:30-08:00",
                            "dayOfWeek":"[Monday,Tuesday,Wednesday,Thursday,Friday]"
                        },
                        "hasMap":{ "@value": "http://www.Californiacourts.gov/District1/CookCounty/map" }
                    },
                    "name": "Cook County - Bridgeview",
                    "publicAccess": true,
                    "subOrganization": {
                        "@context":["http://localhost:8000/data/defs/court-data-definitions.jsonld","http://schema.org"],
                        "@id":"http://www.Californiacourts.gov/District1/CookCounty/Criminal1",
                        "@type":"http://localhost:8000/data/defs/court-data-definitions.jsonld#Courthouse",
                        "contactPoint": {
                            "@context": "http://schema.org/",
                            "@type": "http://schema.org/ContactPoint",
                            "contactType":"Clerk",
                            "description":"Click Clork",
                            "telephone":"(310) 578-9874",
                            "email":"clork.clirk@courts.gov"
                        },
                        "location": {
                            "@context":"http://schema.org/",
                            "@type":"http://schema.org/Place",
                            "address": {
                                "@context":"http://schema.org/",
                                "@type":"http://schema.org/PostalAddress",
                                "streetAddress": "521 Vermont Street Room 504",
                                "addressLocality": "Quincy",
                                "addressRegion": "CA",
                                "postalCode": "62301"
                            },
                            "openingHoursSpecification": {
                                "@context": "http://schema.org/",
                                "@type":"http://schema.org/OpeningHoursSpecification",
                                "opens":"11:30-08:00",
                                "closes":"13:30-08:00",
                                "dayOfWeek":"[Tuesday,Wednesday,Thursday]"
                            }
                        },
                        "mattersServed":"criminal",
                        "name": "Criminal Court of Clark County",
                        "publicAccess": false
                    },
                    "url": { 
                        "@value":"http://www.Californiacourts.gov/District1/CookCounty#website" 
                    }
                }
            }
        }
    }