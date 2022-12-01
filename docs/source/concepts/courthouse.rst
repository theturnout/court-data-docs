Representing Courts and Courthouses
===================================

Court and courthouse information is the primary focus of search queries about courts and thus is the focus of the Court Data Standard. The Standard attempts to identify and make more visible the information that is most commonly sought by the public. In this way, it is hoped that court information will become more accessible to the public and that the burden on court staff to field questions is reduced.

The primary unit of court resources is a courthouse, which may contain individual courts. In the JSON-LD representation of courthouses, courts and courthouses share properties and so a court is expressed as a :code:`subOrganization` of a court. This may not be an accurate depiction of an individual court's relationship to that courthouse, but they are grouped together because they are co-located. Courts can be expressed as completely separate individual entities by removing them from the context of a courthouse. In other words, the court would become the subject of its own JSON-LD file and information about the courthouse would be omitted.

See the :code:`Courthouse` section in the :doc:`Structured Types </dictionary/structured_types>` documentation for more information about the kinds of information that can be recorded using the Court Data Standard.
