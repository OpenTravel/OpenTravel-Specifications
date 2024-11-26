* _ReadMe.txt- This file contains information for all of the documents in the OTA download zip file.

* OTA_CodeTable (folder)
	* OTA_CodeTable20031205.xls- OTA Code Tables in Microsoft Excel format.
	* OTA_CodeTable20031205.xml- OTA Code Tables in XML format.
	* OTA_CodeTable.xsd- OTA XML Schema that are used to validate the OTA Code Tables in XML format.

* OTA2003B_XML (folder)
	* OTA Schema files- OTA XML Schema messages.
	* OTA Instance files- Example XML instance documents in individual files that are taken directly from the OTA_MessageUsersGuide2003BV1.0.pdf.

* OTA2003B_XMLFlattenedSchema (folder)
	* FS_<<filename>>.xsd- OTA XML Schema messages within which the reference(s) to included Schema has been removed.  These Schema are referred to as 'flattened' since only the necessary content from included Schema files has been 'copied' into a message Schema.  For instance, an OTA Schema may include several other Schema files.  The 'flattened' rendition of this same Schema will contain all content from those included Schema files--but only the content that is needed (referenced) by the including Schema.  OTA consumers may find that these 'flattened' Schema provide some performance enhancements when used within an application.

* OTA_MessageUsersGuide2003BV1.0.pdf- The Message Users Guide contains a description of each OTA Message with sample use cases and XML instance documents.  It provides a high-level overview of message functionality.

* OTA_SchemaDesignBestPracticesV3.0.pdf- The OTA XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas.  Typically, this document is used within the OTA to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

* OTA2003BReleaseNotes.pdf- The release notes detail the latest information and changes for any given release.  This file contains detailed documentation on changes made between the 2003A release and the 2003B release. 



============
Special Note
============

Excerpts from the W3C XML Schema Primer:

"In an instance document, the attribute xsi:schemaLocation provides hints from the author to a processor regarding the location of schema documents.  The author warrants that these schema documents are relevant to checking the validity of the document content, on a namespace by namespace basis."

"The schemaLocation attribute contains pairs of values: The first member of each pair is the namespace for which the second member is the hint describing where to find to an appropriate schema document.  The presence of these hints does not require the processor to obtain or use the cited schema documents, and the processor is free to use other schemas obtained by any suitable means, or to use no schema at all."

The intended OTA Schema is listed as the second value in each xsi:schemaLocation in each example instance.  This Schema is available as part of the OTA download.  Please be aware that your individual processors may treat this declaration in a variety of manners (e.g., an absolute path may be required to obtain a valid parse of the example instances).


For more information on xsi:schemaLocation visit http://www.w3.org/TR/xmlschema-0/#schemaLocation


