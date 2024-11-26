OpenTravel 2007A Publication Release Notes


==========================
2007A Publication Contents
==========================
- The following documents are included with 2007A Publication:

----------- OTA_CodeTable (folder) -----------  
- OTA_CodeTable20070613.xls- OpenTravel Code Tables in Microsoft Excel format. 
- OTA_CodeTable20070613.xml- OpenTravel Code Tables in XML format. 
- OTA_CodeTable.xsd- OpenTravel XML Schema that are used to validate the OpenTravel Code Tables in XML format. 

----------- OTA2007A_XML (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 
- XML Instance files- Example XML instance documents in individual files that are taken directly from the OTA_MessageUsersGuide2007AV1.0.pdf.

----------- OTA2007A_XMLFlattenedSchema (folder) -----------  
- FS_<>.xsd- OpenTravel XML Schema messages within which the reference(s) to included Schemas has been removed. These Schemas are referred to as 'flattened' since only the necessary content from included Schema files has been 'copied' into a message Schema. For instance, an OpenTravel Schema may include several other Schema files. The 'flattened' rendition of this same Schema will contain all content from those included Schema files--but only the content that is needed (referenced) by the including Schema. OpenTravel consumers may find that these 'flattened' Schemas provide some performance enhancements when used within an application. 

----------- OTA_MessageUsersGuide2007AV1.0.pdf ----------- 
- The Message Users Guide contains a description of each OpenTravel Message with sample use cases and XML instance documents. It provides a high-level overview of message functionality. This document also contains a table that documents each version change for every XML Schema.

----------- OTA_SchemaDesignBestPracticesV3.04.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases. 

----------- OTA2007AReleaseNotes.pdf ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2006A release and the 2007A release. 


============================
2007A Publication Exclusions
============================
- The following three documents were included in previous publications but are no longer available to the non-member community. These documents have now been subsumed in the new, comprehensive 'OpenTravel Implementation Guide' which is available to OpenTravel member companies only. 

----------- OTA_TransportProtocolReference_HTTPV1.0.pdf ----------- 
- This document contains guidance that describes how implementers should use HTTP (Hypertext Transfer Protocol) in regards to OpenTravel message exchange.

----------- OTA_ImplementationGuide_WSDLV1.0.pdf ----------- 
- This document contains best practices for building WSDL (Web Services Description Language) files for use with the OpenTravel specification.

----------- OTA_TransportProtocolReference_SOAPV1.0.pdf ----------- 
- This document contains guidance that describes how implementers should use SOAP (Simple Object Access Protocol) in regards to OpenTravel message exchange. These guidelines include best practices for areas such as message structure, transport method (RPC vs. messaging), error handling, SOAP security and SOAP attachments. Specifications of transport protocols has not formally been a part of the OpenTravel Specifications, and this document is intended to bridge the gap between the OpenTravel specifications and the SOAP specification.


======================
Discontinued Resources
======================
- For the 2006A publication and publications previous to that, OpenTravel provided a reference guide described as follows: "an auto-generated set of web pages that allow the display of and navigation through the annotations within the XML Schemas. It provides documentation at the “field-level” detailing the use of individual elements and attributes."
- This reference guide is still available for 2006A and previous (at http://www.opentravel.org/Specifications/XsdDoc.aspx) but is no longer supported due to lack of support by the vendor of the utility that was used to create these reference pages. 


========================
New/Updated XML Messages
========================
- No new messages have been created for the 2007A Publication.
- Based on the 2007A Project Team Proposals the following Schemas have been updated:

----------- OTA_HotelRatePlanNotifRQ -----------
- This message was extended by adding a new <Offers> element which permits a precise description of promotional offers together with the booking conditions under which they apply. 

- It is important to note that numerous other changes have been made in the 2007A publication based on comments received. These changes are documented in the 'OTA2007AReleaseNotes.pdf' document cited above.


============
Special Note
============
- Excerpts from the W3C XML Schema Primer:

"In an instance document, the attribute xsi:schemaLocation provides hints from the author to a processor regarding the location of schema documents. The author warrants that these schema documents are relevant to checking the validity of the document content, on a namespace by namespace basis."

"The schemaLocation attribute contains pairs of values: The first member of each pair is the namespace for which the second member is the hint describing where to find to an appropriate schema document. The presence of these hints does not require the processor to obtain or use the cited schema documents, and the processor is free to use other schemas obtained by any suitable means, or to use no schema at all."

The intended OpenTravel Schema is listed as the second value in each xsi:schemaLocation in each example instance. This Schema is available as part of the OpenTravel download. Please be aware that your individual processors may treat this declaration in a variety of manners (e.g., an absolute path may be required to obtain a valid parse of the example instances).
