Structured Types
================

In the context of the vocabulary of Schema.org, a structured type refers to the overall category of entity or thing being described. In programming, this would be similar to a class. The Court Data Standard is composed of a combination of existing types as well as some that have been created to accommodate data related to courts.

Each property listed in the section following this one is used by one or more types to describe its subject. Properties may be shared between different types (e.g., a courthouse, a person, and a court system may all have a “name”). The section below describes the types included in the Court Data Standard as well as the properties associated with them.

Properties and types can be textually distinguished by their casing: properties are recorded with camelCase while types are recorded with PascalCase.

AdministrativeArea
~~~~~~~~~~~~~~~~~~

**Description:** A geographical region, typically under the jurisdiction
of a particular government organization.

**Associated Properties:**

-  :ref:`areaServed <dictionary/properties:area served>`

-  :ref:`containsPlace <dictionary/properties:local court>`

-  :ref:`geoContains <dictionary/properties:composing administrative area>`

-  :ref:`name <dictionary/properties:name>`

ContactPoint
~~~~~~~~~~~~

**Description:** A person or resource which can be reached by members of
the public for information about the courthouse or the services it
offers.

**Associated Properties:**

-  :ref:`contactType <dictionary/properties:contact type>`

-  :ref:`description <dictionary/properties:contact name>`

-  :ref:`email <dictionary/properties:contact email>`

-  :ref:`telephone <dictionary/properties:contact telephone>`

Courthouse
~~~~~~~~~~

**Description:** A public building in which legal matters are conducted,
especially those involving courts and judges or other officials.

**Associated Properties:**

-  :ref:`areaServed <dictionary/properties:area served>`

-  :ref:`conditionsOfAccess <dictionary/properties:conditions of access>`

-  :ref:`contactPoint <dictionary/properties:contact point>`

-  :ref:`hasOfferCatalog <dictionary/properties:has amenities>`

-  :ref:`image <dictionary/properties:courthouse image>`

-  :ref:`knowsLanguage <dictionary/properties:languages spoken>`

-  :ref:`location <dictionary/properties:location>`

-  :ref:`mattersServed <dictionary/properties:matters served>`

-  :ref:`name <dictionary/properties:name>`

-  :ref:`publicAccess <dictionary/properties:open to public>`

-  :ref:`suborganization <dictionary/properties:court>`

-  :ref:`url <dictionary/properties:court webpage>`

-  :ref:`requiresArrangement <dictionary/properties:features requiring arrangement>`

CourtSystem
~~~~~~~~~~~

**Description:** A local, regional, or national organization of courts
and courthouses.

**Associated Properties:**

-  :ref:`areaServed <dictionary/properties:area served>`

-  :ref:`geoContains <dictionary/properties:composing administrative area>`

-  :ref:`containsPlace <dictionary/properties:local court>`

-  :ref:`name <dictionary/properties:name>`

OfferCatalog
~~~~~~~~~~~~

**Description:** A collection of lists of items that contains
information about amenities.

**Associated Properties:**

-  :ref:`itemListElement <dictionary/properties:amenities offered>`

OpeningHoursSpecification
~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:** The hours and days of the week during which the
courthouse is open to the public.

**Associated Properties:**

-  :ref:`closes <dictionary/properties:close time>`

-  :ref:`dayOfWeekdayOfWeek <dictionary/properties:open days>`

-  :ref:`opens <dictionary/properties:open time>`

Place
~~~~~

**Description:** Entities that have a somewhat fixed, physical
extension.

**Associated Properties:**

-  :ref:`address <dictionary/properties:address>`

-  :ref:`openingHoursSpecification <dictionary/properties:business hours>`

-  :ref:`hasMap <dictionary/properties:map url>`

PostalAddress
~~~~~~~~~~~~~

**Description:** The physical address at which the courthouse is
located.

**Associated Properties:**

-  :ref:`addressLocality <dictionary/properties:city>`

-  :ref:`addressRegion <dictionary/properties:state>`

-  :ref:`postalCode <dictionary/properties:zip code>`

-  :ref:`streetAddress <dictionary/properties:street address>`
