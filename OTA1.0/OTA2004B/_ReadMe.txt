* _ReadMe.txt- This file contains information for all of the documents in the OTA download zip file.

* OTA_CodeTable (folder)
	* OTA_CodeTable20041203.xls- OTA Code Tables in Microsoft Excel format.
	* OTA_CodeTable20041203.xml- OTA Code Tables in XML format.
	* OTA_CodeTable.xsd- OTA XML Schema that are used to validate the OTA Code Tables in XML format.

* OTA2004B_XML (folder)
	* OTA Schema files- OTA XML Schema messages.
	* OTA Instance files- Example XML instance documents in individual files that are taken directly from the OTA_MessageUsersGuide2004BV1.0.pdf.

* OTA2004B_XMLFlattenedSchema (folder)
	* FS_<<filename>>.xsd- OTA XML Schema messages within which the reference(s) to included Schemas has been removed.  These Schemas are referred to as 'flattened' since only the necessary content from included Schema files has been 'copied' into a message Schema.  For instance, an OTA Schema may include several other Schema files.  The 'flattened' rendition of this same Schema will contain all content from those included Schema files--but only the content that is needed (referenced) by the including Schema.  OTA consumers may find that these 'flattened' Schemas provide some performance enhancements when used within an application.

* 2001-1029-2001C_Infrastructure.doc- The Implementation Infrastructure Guidelines, last published in 2001C as 
“Infrastructure Specification”, provides information about how to implement the transport and enveloping layers for the purpose of sending and receiving OTA messages between systems. At present only information for the ebXML Message Service is documented. Definition of the mapping to alternative infrastructure technologies is currently under development.

* OTA_MessageUsersGuide2004BV1.0.pdf- The Message Users Guide contains a description of each OTA Message with sample use cases and XML instance documents.  It provides a high-level overview of message functionality.

* OTA_SchemaDesignBestPracticesV3.02.pdf- The OTA XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas.  Typically, this document is used within the OTA to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

* OTA2004BReleaseNotes.pdf- The release notes detail the latest information and changes for any given release.  This file contains detailed documentation on changes made between the 2004A release and the 2004B release. 

* OTA_Sponsors.pdf- This file contains special thanks to OTA sponsors.

** Also available via the Internet is a Reference Guide, which is an auto-generated set of web pages that allow the display of and navigation through the annotations within the XML Schemas.  It provides documentation at the “field-level” detailing the use of individual elements and attributes. This is available at http://www.opentravel.org/2004B/ using the link OTA 2004B XSDdoc.


============
Special Note
============

Excerpts from the W3C XML Schema Primer:

"In an instance document, the attribute xsi:schemaLocation provides hints from the author to a processor regarding the location of schema documents.  The author warrants that these schema documents are relevant to checking the validity of the document content, on a namespace by namespace basis."

"The schemaLocation attribute contains pairs of values: The first member of each pair is the namespace for which the second member is the hint describing where to find to an appropriate schema document.  The presence of these hints does not require the processor to obtain or use the cited schema documents, and the processor is free to use other schemas obtained by any suitable means, or to use no schema at all."

The intended OTA Schema is listed as the second value in each xsi:schemaLocation in each example instance.  This Schema is available as part of the OTA download.  Please be aware that your individual processors may treat this declaration in a variety of manners (e.g., an absolute path may be required to obtain a valid parse of the example instances).


For more information on xsi:schemaLocation visit http://www.w3.org/TR/xmlschema-0/#schemaLocation


