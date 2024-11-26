


OTA 2005B Publication Release Notes


The following documents are included with 2005B Publication:

OTA_CodeTable (folder) 
	OTA_CodeTable20051122.xls- OTA Code Tables in Microsoft Excel format. 
	OTA_CodeTable20051122.xml- OTA Code Tables in XML format. 
	OTA_CodeTable.xsd- OTA XML Schema that are used to validate the OTA Code Tables in XML format. 

OTA2005B_XML (folder) 
	OTA Schema files- OTA XML Schema messages. 
	OTA Instance files- Example XML instance documents in individual files that are taken directly from the OTA_MessageUsersGuide2005BV1.0.pdf.

OTA2005B_XMLFlattenedSchema (folder) 
	FS_<>.xsd- OTA XML Schema messages within which the reference(s) to included Schemas has been removed. These Schemas are referred to as 'flattened' since only the necessary content from included Schema files has been 'copied' into a message Schema. For instance, an OTA Schema may include several other Schema files. The 'flattened' rendition of this same Schema will contain all content from those included Schema files--but only the content that is needed (referenced) by the including Schema. OTA consumers may find that these 'flattened' Schemas provide some performance enhancements when used within an application. 

OTA_MessageUsersGuide2005BV1.0.pdf- The Message Users Guide contains a description of each OTA Message with sample use cases and XML instance documents. It provides a high-level overview of message functionality. 

OTA_SchemaDesignBestPracticesV3.03.pdf- The OTA XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OTA to ensure that the creation of XML Schemas is consistent in design across the organization and across releases. 

OTA2005BReleaseNotes.pdf- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2004B release and the 2005B release. 

OTA_Sponsors.pdf- This file contains special thanks to OTA sponsors. 

OTA_TransportProtocolReference_HTTPV1.0.doc- This document contains guidance that describes how implementers should use HTTP in regards to OTA message exchange.

** Also available via the Internet is a Reference Guide, which is an auto-generated set of web pages that allow the display of and navigation through the annotations within the XML Schemas. It provides documentation at the “field-level” detailing the use of individual elements and attributes. This is available at http://www.opentravel.org/2005B/ using the link OTA 2005B XSDdoc. 

============
Special Note
============

Excerpts from the W3C XML Schema Primer:

"In an instance document, the attribute xsi:schemaLocation provides hints from the author to a processor regarding the location of schema documents. The author warrants that these schema documents are relevant to checking the validity of the document content, on a namespace by namespace basis."

"The schemaLocation attribute contains pairs of values: The first member of each pair is the namespace for which the second member is the hint describing where to find to an appropriate schema document. The presence of these hints does not require the processor to obtain or use the cited schema documents, and the processor is free to use other schemas obtained by any suitable means, or to use no schema at all."

The intended OTA Schema is listed as the second value in each xsi:schemaLocation in each example instance. This Schema is available as part of the OTA download. Please be aware that your individual processors may treat this declaration in a variety of manners (e.g., an absolute path may be required to obtain a valid parse of the example instances).




Based on the 2005B Project Team Proposals the following Schemas have been created or updated:


OTA_HotelRFP_Meeting- Based on a review of the Convention Industry Council's (APEX) initiative requirements, enhancements were made the hotel RFP meeting messages. The hotel work group made every effort to ensure these enhancements did not break backward compatibility with the previously existing RFP meeting messages.

OTA_VehExchange- This is a new message intended to be used for the physical exchange of a vehicle.

OTA_Cruise messages- Eight message sets are being released for cruise. This release contains SailingAvailability, FareAvailability, CategoryAvailability, CabinAvailability, CabinHold, CabinUnhold, PriceBooking and CreateBooking.

OTA_NotifReport- An initial requirement in the hotel work group to create a message for an asynchronous update report led to the creation of a generic message that can have added functionally as needed. In this release functionally has been added for reports on Hotel Availability Status and Hotel Rate Amount messages.

OTA_FileAttachment- OTA generic messages that enable sending encoded binary files (e.g., image files, videos, etc) to a receiver that will either store or process these files. When trying to send a binary file encoded in a SOAP message, the entire message is encoded and sent, usually broken up into segments. The receiver then needs to decode each segment and recompose the content sent. Having a common message listing the files sent and their attributes enables or facilitates this decoding. These messages specify each file attached and define all required attributes required by the receiver to decode the encoded message and reconstruct the files at its end. Support for file attachments has also been added in the HotelContentDescription Schema by way of the MultimediaObjectType complexType.





