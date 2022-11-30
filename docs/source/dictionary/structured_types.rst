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

-  `contactType <#contact-type>`__

-  `description <#contact-name>`__

-  `email <#contact-email>`__

-  `telephone <#telephone>`__

Courthouse
~~~~~~~~~~

**Description:** A public building in which legal matters are conducted,
especially those involving courts and judges or other officials.

**Associated Properties:**

-  `areaServed <#area-served>`__

-  `conditionsOfAccess <#conditions-of-access>`__

-  `contactPoint <#contactpoint>`__

-  `hasOfferCatalog <#has-amenities>`__

-  `image <#courthouse-image>`__

-  `knowsLanguage <#languages-spoken>`__

-  `location <#location>`__

-  `mattersServed <#matters-served>`__

-  `name <#name>`__

-  `publicAccess <\l>`__

-  `suborganization <#court>`__

-  `url <#court-webpage>`__

-  `requiresArrangement <#features-requiring-arrangement>`__

CourtSystem
~~~~~~~~~~~

**Description:** A local, regional, or national organization of courts
and courthouses.

**Associated Properties:**

-  `areaServed <#area-served>`__

-  `geoContains <#composing-administrative-area>`__

-  `containsPlace <#local-court>`__

-  `name <#name>`__

OfferCatalog
~~~~~~~~~~~~

**Description:** A collection of lists of items that contains
information about amenities.

**Associated Properties:**

-  `itemListElement <#amenities-offered>`__

OpeningHoursSpecification
~~~~~~~~~~~~~~~~~~~~~~~~~

**Description:** The hours and days of the week during which the
courthouse is open to the public.

**Associated Properties:**

-  `closes <#close-time>`__

-  `dayOfWeekdayOfWeek <#open-days>`__

-  `opens <#open-time>`__

Place
~~~~~

**Description:** Entities that have a somewhat fixed, physical
extension.

**Associated Properties:**

-  `address <#address>`__

-  `openingHoursSpecification <#openinghoursspecification>`__

-  `hasMap <#map-url>`__

PostalAddress
~~~~~~~~~~~~~

**Description:** The physical address at which the courthouse is
located.

**Associated Properties:**

-  `addressLocality <#city>`__

-  `addressRegion <#state>`__

-  `postalCode <#postalCode>`__

-  `streetAddress <#street-address>`__
