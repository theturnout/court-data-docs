Properties and Definitions
==========================

address
~~~~~~~

**Property Name**: *address*
**Expected Value/Type**: `PostalAddress <#postaladdress>`__
**Description**: The physical address of the courthouse made up of street address, city, state, and zip code.

amenities offered
~~~~~~~~~~~~~~~~~

**Property Name**: *itemListElement*
**Expected Value/Type**: Text
**Description**: A list of amenities offered to the public at the courthouse. Each amenity should be separated by a comma and whitespace.

.. code-block:: json-ld

    "itemListElement": "e-filing kiosk, internet, public restrooms, waiting area"

area served
~~~~~~~~~~~

**Property Name**: *areaServed*
**Expected Value/Type**: `AdministrativeArea <#administrativearea>`__
**Description**: A representation of the geographic area served by a Courthouse or a CourtSystem. When used by a CourtSystem, the areaServed may point to one or more AdministrativeAreas to represent geographic divisions of the court, e.g., districts and circuits.

business hours
~~~~~~~~~~~~~~

**Property Name**: *openingHoursSpecification*
**Expected Value/Type**: `OpeningHoursSpecification <#openinghoursspecification>`__
**Description**: The days and times during which the court or courthouse operates.

city
~~~~

**Property Name**: *addressLocality*
**Expected Value/Type**: Text
**Description**: The city portion of the courthouse's physical address.

.. code-block:: json-ld

    "addressLocality": "Albuquerque"

close time
~~~~~~~~~~

**Property Name**: *closes*
**Expected Value/Type**: Datetime
**Description**: The time at which the court or courthouse ceases operation.

.. code-block:: json-ld

    "closes": "16:30-08:00"

composing administrative area
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Property Name**: *geoContains*
**Expected Value/Type**: `AdministrativeArea <#administrativearea>`__
**Description**: The AdministrativeArea(s) contained in the AdministrativeArea being described.

conditions of access
~~~~~~~~~~~~~~~~~~~~

**Property Name**: *conditionsOfAccess*
**Expected Value/Type**: Text
**Description**: A list of items required for entry to a court or courthouse (such as identification) and items prohibited from being carried into the court or courthouse (such as cell phones or cameras). The first element of a list of required items must be "required" while the first element of a list of prohibited items must be "prohibited". Required and prohibited items should be recorded in the same instance of this property.

.. code-block:: json-ld

"conditionsOfAccess": "required, identification, prohibited, cell phones, cameras”

contact email
~~~~~~~~~~~~~

**Property Name**: *email*
**Expected Value/Type**: Text
**Description**: The email address at which a person, service or department associated with the court or courthouse may be reached.

.. code-block:: json-ld

    "email": "guy.smiley@courts.ca.gov"

contact name
~~~~~~~~~~~~

**Property Name**: *description*

**Expected Value/Type**: Text
**Description**: The name and title of the person with whom the contact information is associated. If the number or email address leads to an automated message or a line that no one person is responsible for answering the value “NA” must be entered.

.. code-block:: json-ld

    "description": "John Smith, Circuit Clerk"

.. code-block:: json-ld

    "description": "NA"

contact point
~~~~~~~~~~~~~

**Property Name**: *contactPoint*
**Expected Value/Type**: `ContactPoint <#contactpoint>`__
**Description**: A telephone number and/or email address at which court/courthouse staff or resources may be reached by members of the public.

contact telephone
~~~~~~~~~~~~~~~~~

**Property Name**: *telephone*
**Expected Value/Type**: Text
**Description**: The phone number at which a person, service, or department associated with the court or courthouse may be reached. It must be expressed in ten-digit format with the area code enclosed in parentheses, a whitespace between the area code and first group of digits, and a dash between the second and third group of digits.

.. code-block:: json-ld

    "telephone": "(679) 574-6314"

contact type
~~~~~~~~~~~~

**Property Name**: *contactType*
**Expected Value/Type**: Text
**Description**: The title or function of the service, department, or person with whom the contact information is associated.

.. code-block:: json-ld

    "contactType": "General Court Information"

.. code-block:: json-ld

    "contactType": "Court Accessibility Coordinator"

.. code-block:: json-ld

    "contactType": "Jury Service"

court
~~~~~

**Property Name**: *subOrganization*
**Expected Value/Type**: `Courthouse <#courthouse>`__
**Description**: Records information about courts located within a courthouse such as hours of operation, court-specific contact information, and matters served.

court webpage 
~~~~~~~~~~~~~

**Property Name**: *url*
**Expected Value/Type**: URL
**Description**: A URL to the webpage of the courthouse.

.. code-block:: json-ld

    "url": "https://www.cookcountycourt.org/ABOUT-THE-COURT/Municipal-Department/Fifth-Municipal-District-Bridgeview"

courthouse image
~~~~~~~~~~~~~~~~

**Property Name**: *image*
**Expected Value/Type**: URL
**Description**: A URL linking directly to an image of the courthouse.

.. code-block:: json-ld

    "image": "https://www.cookcountycourt.org/ABOUT-THE-COURT/Municipal-Department/Fifth-Municipal-District-Bridgeview/image.png"

features requiring arrangement
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Property Name**: *requiresArrangement*
**Expected Value/Type**: Text
**Description**: A list of all services and/or features available at this building or location that require arrangement in advance.

.. code-block:: json-ld

    "requiresArrangement": "staircase lift, Spanish language interpreter"

has amenities
~~~~~~~~~~~~~

**Property Name**: *hasOfferCatalog*
**Expected Value/Type**: `OfferCatalog <#offercatalog>`__  
**Description**: An indicator that a courthouse offers amenities to the public, such as free wifi, public restrooms, etc.

languages spoken
~~~~~~~~~~~~~~~~

**Property Name**: *knowsLanguage*
**Expected Value/Type:** Text
**Description:** The language or languages spoken or that may be accommodated at the courthouse. Languages must be expressed with `ISO 639-1 compliant <https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes>`__ two-character codes. If multiple languages are accommodated, they should be recorded as a list with a comma and whitespace separating languages.

.. code-block:: json-ld

    "knowsLanguage": "en, es"

local court
~~~~~~~~~~~

**Property Name**: *containsPlace*
**Expected Value/Type**: `Courthouse <#courthouse>`__
**Description**: The courthouse(s) in the AdministrativeArea. This property is only expected for the highest granularity administrative areas, i.e., the administrative areas that have no geoContains property.

location
~~~~~~~~

**Property Name**: *location*
**Expected Value/Type**: `Place <#place>`__
**Description**: Information about the courthouse including physical address, operating hours, and a map.

map URL
~~~~~~~

**Property Name**: *hasMap*
**Expected Value/Type**: URL
**Description**: A URL to a webpage containing a map that indicates the courthouse's physical location.

.. code-block:: json-ld

    "hasMap": "https://www.cookcountycourt.org/ABOUT-THE-COURT/Municipal-Department/Fifth-Municipal-District-Bridgeview"

matters served
~~~~~~~~~~~~~~

**Property Name**: *mattersServed*
**Expected Value/Type**: Text
**Description**: A list indicating the types of cases heard by a court or generally within a courthouse.

.. code-block:: json-ld

    "mattersServed": "family and custody, traffic infractions, small claims"

name
~~~~

**Property Name**: *name*
**Expected Value/Type**: Text
**Description**: The official name of the entity being described. This may be associated with an administrative area, person, system, or courthouse.

.. code-block:: json-ld

    "name": "State of Illinois Circuit Court System”

.. code-block:: json-ld

    "name": "Cook County: Fifth Municipal District - Bridgeview Courthouse"

open days
~~~~~~~~~

**Property Name**: *dayOfWeek*
**Expected Value/Type**: Text
**Description**: A text list of the days of the week during which the courthouse is open to the public. These must be spelled out in full and not abbreviated. Days must be separated by a comma and whitespace.


.. code-block:: json-ld

    "dayOfWeek": "Monday, Tuesday, Wednesday, Thursday, Friday"

open time
~~~~~~~~~

**Property Name**: *opens*
**Expected Value/Type**: DateTime.
**Description**: The time at which the court or courthouse begins operations.

.. code-block:: json-ld

    "opens": "09:00-08:00"

open to public
~~~~~~~~~~~~~~

**Property Name**: *publicAccess*
**Expected Value/Type**: Text
**Description**: Indicates whether a court or courthouse is accessible to members of the public who do not have official business (e.g., observers of a proceeding or members of the press). Values for this property must be either "True" or "False".

.. code-block:: json-ld

    "publicAccess":"True"

state
~~~~~

**Property Name**: *addressRegion*
**Expected Value/Type**: Text
**Description**: The state portion of the courthouse's physical address. This must be a two-character state abbreviation.

.. code-block:: json-ld

    "addressRegion": "NM"

street address
~~~~~~~~~~~~~~

**Property Name**: *streetAddress*
**Expected Value/Type**: Text
**Description**: The street address portion of the courthouse's physical address. Abbreviations must be expanded.

.. code-block:: json-ld

"streetAddress": "123 Main Street"

zip code
~~~~~~~~

**Property Name**: *postalCode*
**Expected Value/Type**: Text
**Description**: The zip code portion of the courthouse's physical address. This must be a five-digit number.


.. code-block:: json-ld

    "postalCode": "62301"