2001C OTA Specification

These are the contents of the 2001C OTA Specification:

· Specification Document- MS Word or .pdf file that contains the traditional specification information; along with introduction and explanations of the business content.

· XML Schema and Schema Fragments - All OTA XML Schema files are in conformance with the World-Wide Web Consortium (W3C) Recommendation XML Schema 1.0.*

· XML Instance Documents - Included in the 2001C Specification are sample XML instance files that have been validated to OTA XML Schema files.

Here are the W3C XML Schema files for the 2001C OTA Specification.  Included within its own folder are the Generic XML Schema files and Sample instance documents for most of the OTA XML Schema files.  For some RQ/RS message pairs, there are more than one instance document example.   

* While the text of the Specification document makes every attempt to accurately reflect the XML Schema, in the case of a conflict, the XML Schema takes precedence.


Changes to 2001B Specifications
================================
OTA_CancelRS - Changed CancelRules to be optional (minOccurs="0").  Moved UniqueID & CancelRules down to apply to both Sucess and Error and not impact structure.  Added "include OTA_POS.xsd".  Added element ref POS with minOccurs="0" at the end of this sequence.

OTA_POS - UniqueID ref within element Source container is now constrained to maxOccurs="5".

OTA_v2ent - Added an optional attribute <xs:attribute name="NodeList"> to capture the XPath statement of the offending data back to requesting system
