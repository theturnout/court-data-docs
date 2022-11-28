Data Types
==========

The Court Data Standard requires values to be of a specific predefined
type for each property. This facilitates standardization, consistency,
and ease of automated collection of court data. An explanation of data
types follows below.

Text
----

Text (also known as a string) is a sequence of characters. Be sure to
read the description for each text property, as some properties only
allow values that are formatted in a specific manner. Text values must
be free of leading or trailing whitespace.

URL
---

A Uniform Resource Locator (URL) is a unique sequence of characters that
identifies the location of resources on the web, most commonly websites.
https://www.google.com is an example of a URL.

DateTime
--------

A DateTime is an expression of a date and/or time in an
`ISO-8601 <https://en.wikipedia.org/wiki/ISO_8601>`__ compliant format.
For the purposes of this standard, only the time portion of a DateTime
value is required. **Time must be expressed in four-digit 24-hour format
with hours and minutes separated by a colon (:)**. The time zone must also
be indicated by appending a plus or minus symbol (+, -) and the GMT
offset immediately after the minutes (e.g., 9:00 AM PST would be
expressed as 09:00-08:00).