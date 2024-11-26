=============================================
OPENTRAVEL 2009A README
=============================================

Important Notice: OpenTravel has removed all default values from the specification for the 2009A publication; please refer to the included 2009A Release Notes document for additional information.

=============================
2009A Publication Contents
=============================

- The following documents are included with 2009A Publication:

----------- OpenTravel_CodeTable (folder) -----------  
- OpenTravel_CodeTable20090615.xls- OpenTravel Code Tables in Microsoft Excel format. 
- OpenTravel_CodeTable20090615.xml- OpenTravel Code Tables in XML format. 
- OpenTravel_CodeTable.xsd- OpenTravel XML Schema that are used to validate the OpenTravel Code Tables in XML format. 

----------- OpenTravel2009A_XML (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 
- XML Instance files- Example XML instance documents in individual files that are taken directly from the OpenTravel_MessageUserGuide_2009A.pdf.

----------- OpenTravel2009A_XMLFlattenedSchema (folder) -----------  
- FS_<>.xsd- OpenTravel XML Schema messages within which the reference(s) to included Schemas has been removed. These Schemas are referred to as 'flattened' since only the necessary content from included Schema files has been 'copied' into a message Schema. For instance, an OpenTravel Schema may include several other Schema files. The 'flattened' rendition of this same Schema will contain all content from those included Schema files--but only the content that is needed (referenced) by the including Schema. OpenTravel consumers may find that these 'flattened' Schemas provide some performance enhancements when used within an application. 

----------- OpenTravel_MessageUsersGuide_2009A.pdf ----------- 
- The Message Users Guide contains a description of each OpenTravel Message with sample use cases and XML instance documents. It provides a high-level overview of message functionality. This document also contains a table that documents each version change for every XML Schema.

----------- OpenTravel_SchemaDesignBestPracticesV3.07.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases. 

----------- OpenTravel_ReleaseNotes_2009A.pdf ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2008B release and the 2009A release. 


----------- OpenTravel_ImplementationGuide_v1.1_ExecSum.pdf --------------
- This is an executive summary of the OpenTravel Implementation Guide. The purpose of the OpenTravel Implementation Guide is to provide invaluable information to both analysts and implementers of the OpenTravel specification on how to more easily understand and build software systems that are interoperable with other travel systems using the OpenTravel schema. The full Guide is available to members of the OpenTravel Alliance via the Wiki http://wiki.opentravel.org/index.php/Public:Resources.

=====================================
2009A New Schemas and Schema Updates
=====================================

- OTA_HotelAvailGetRQ/RS.xsd: Provides the ability to request availability details for hotel properties by specific criteria that may include dates, date ranges, rates, rooms and products.  
- OTA_HotelInvBlockRQ/RS.xsd: Provides the ability to request inventory block details for hotel properties by specific criteria that may include dates, date ranges, rooms and products. 
- OTA_HotelInvCountRQ/RS.xsd: Provides the ability to request inventory count details for hotel properties by specific criteria that may include dates, date ranges, rooms and products. 
- OTA_ProfileMergeRQ/RS.xsd: Provides for the merging of one or more profiles.
- OTA_ProfileModifyRQ/RS.xsd: Provides for modifying a profile identified by UniqueID. It is used for a full overlay of the profile. 
- OTA_VehResStatusNotifRQ/RS.xsd: Provides the ability to inform a trading partner of a confirmation or an update of an existing reservation.

- The Air and Authorization messages have a number of updates based on submitted comments. 


======================================================
OpenTravel Implementation Guide Available for Members
======================================================

OpenTravel has published an Implementation Guide that provides, in a single document, information that an implementer of the OpenTravel specification can use to more easily build software systems that are interoperable with other travel systems. The guide also should be useful for analysts who need to understand how to use the OpenTravel specification. In addition, it will help promote the adoption of the specification by members who have never implemented XML schemas or who are just becoming involved with OpenTravel.  The OpenTravel Implementation Guide is available to members through the OpenTravel wiki. Recent additions include a section on Reliable Messaging authored by Gee Chia of IBM.

======================================
Deprecation Warning
======================================
Based on a comment received in early 2008, OpenTravel has implemented a new design best practice to not use default values in its specification. Based on this new best practice, OpenTravel has removed all default values in its 2009A publication. 

======================
New Resource Available
======================
The OpenTravel Model Viewer, built in conjunction with PilotFish Technology, is a schema documentation application that transforms plain XML schema files into cross-referenced, hyperlinked HTML documents and provides a detailed functional report for each schema component. Sample files, code lists, and additional documentation are also seamlessly integrated into this comprehensive browser-based utility. The OpenTravel Model Viewer makes it effortless to navigate through a large collection of XML vocabulary.

URL:
http://www.opentravel.org/Specifications/ModelViewer.aspx

======================================
Other Resources
======================================
Comments may be submitted at any time and members can view the Comments Tracking Spreadsheet at http://wiki.opentravel.org/index.php/Member:CommentsSpreadsheet to track current and resolved comments.

============
Special Note
============
- Excerpts from the W3C XML Schema Primer:

"In an instance document, the attribute xsi:schemaLocation provides hints from the author to a processor regarding the location of schema documents. The author warrants that these schema documents are relevant to checking the validity of the document content, on a namespace by namespace basis."

"The schemaLocation attribute contains pairs of values: The first member of each pair is the namespace for which the second member is the hint describing where to find to an appropriate schema document. The presence of these hints does not require the processor to obtain or use the cited schema documents, and the processor is free to use other schemas obtained by any suitable means, or to use no schema at all."

The intended OpenTravel Schema is listed as the second value in each xsi:schemaLocation in each example instance. This Schema is available as part of the OpenTravel download. Please be aware that your individual processors may treat this declaration in a variety of manners (e.g., an absolute path may be required to obtain a valid parse of the example instances).