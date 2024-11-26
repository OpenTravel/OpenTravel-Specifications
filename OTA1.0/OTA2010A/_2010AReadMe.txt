=============================================
OPENTRAVEL 2010A README
=============================================

=============================
2010A Publication Contents
=============================

- The following documents are included with the OpenTravel 2010A Publication:

----------- OpenTravel_CodeTable (folder) -----------  
- OpenTravel_CodeTable20100322.xls- OpenTravel Code Tables in Microsoft Excel format. 
- OpenTravel_CodeTable20100322.xml- OpenTravel Code Tables in XML format. 
- OpenTravel_CodeTable.xsd- OpenTravel XML Schema that are used to validate the OpenTravel Code Tables in XML format.

----------- OpenTravel2010A_XML (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 
- XML Instance files- Example XML instance documents in individual files that are taken directly from the use cases in the OpenTravel_MessageUserGuide_2010A.pdf.

----------- OpenTravel_MessageUsersGuide_2010A.pdf ----------- 
- The Message Users Guide (MUG) contains a description of each OpenTravel Message with sample use cases and links to XML instance documents. It provides a high-level overview of message functionality. In March of 2010, in conjunction with the 2010A Publication, the OpenTravel Message Users Guide is significantly redesigned (and streamlined) to support all cycles of an OpenTravel-enabled system implementation, from design to system testing. In addition to updated message descriptions, the new Message Users Guide provides:
	-A point-and-click index of business functionality and use cases for each message, allowing an implementer to quickly identify the OpenTravel messages that suit their own and their trading partner business requirements,
	-Links to each message (summarized) data dictionary that allow implementers to see the names and descriptions of elements and attributes in a message and the enumeration values where applicable,
	-Extended message scenario use cases that help implementers understand the range of business scenarios that can be accomplished per message,
	-A new “Introduction and Getting Started” section that includes links to OpenTravel implementer/member resources, OpenTravel schema architecture basics, and links to all third party standards referenced in OpenTravel messages, such as ABTA, IATA and ISO standards to help implementers understand the relationships between OpenTravel messages and other third party standards, and,
	-Point-and-click access to online message sample use case instances that allow an implementer to access only the sample instances they require (note that these instances were not intended for production use by implementers, but rather for human reference.)

----------- OpenTravel_MessageXSDVersioningTable_2010A.pdf ----------- 
- OpenTravel began tracking versions in the 2003B release cycle. Prior to the 2008A release, the version table contained 2001 and 2002 data for newly created messages. This document contains a table with each OpenTravel message version from 2003B through 2010A. This document may also be found on the OpenTravel wiki in the "Implementation" section on the main page (http://wiki.opentravel.org/index.php/Main_Page).

----------- OpenTravel_SchemaDesignBestPracticesV3.08.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

----------- OpenTravel_ReleaseNotes_2010A.pdf ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2009A release and the 2010A release. 

----------- OpenTravel_ImplementationGuide_v1.2_ExecSum.pdf --------------
- This is an executive summary of the OpenTravel Implementation Guide. The purpose of the OpenTravel Implementation Guide is to provide invaluable information to both analysts and implementers of the OpenTravel specification on how to more easily understand and build software systems that are interoperable with other travel systems using the OpenTravel schema. The full Guide is available to members of the OpenTravel Alliance via the Wiki http://wiki.opentravel.org/index.php/Public:Resources.

=========================================
2010A New Schemas and Significant Schema Updates
=========================================

- OTA_VehResNotifRQ/RS.xsd: These new messages address a common vehicle rental business need to be able to bulk transfer entire reservations between computer systems. Existing OpenTravel messages support requesting new reservations and retrieving existing reservation information in a client/server style pull operation, however, they do not support transferring bulk reservation information in a notification style push operation like the new messages do. The new messages provide bulk transfers of vehicle reservations, supporting system notification of changes made to reservations on another system so the two systems can be kept in sync with each other.

- Dynamic Package Message Enhancements: The Dynamic Package messages provide a central location for component searches to be run simultaneously via one message and are functionally different from the existing OpenTravel Package messages. Rather than operating on static packages with pre-determined components, the Dynamic Package messages provide the functionality to create packages with independent component selections. Previously, the dynamic package messages contained only two component types: air and hotel. With the 2010A standard, support has been added for two additional component types:
	-Rental Car – this allows dynamic packages to include rental cars
	-Package Option – these can be added to a package as either stand-alone products or as included items to existing components. Examples of package options include: show tickets, amusement park tickets, airport transfers, meal plan vouchers, club passes and travel insurance.

======================================================
OpenTravel Implementation Guide Available for Members
======================================================

OpenTravel has published an Implementation Guide that provides, in a single document, information that an implementer of the OpenTravel specification can use to more easily build software systems that are interoperable with other travel systems. The guide also should be useful for analysts who need to understand how to use the OpenTravel specification. In addition, it will help promote the adoption of the specification by members who have never implemented XML schemas or who are just becoming involved with OpenTravel.  The OpenTravel Implementation Guide is available to members through the OpenTravel wiki.

======================
New Resource Available
======================

- The OpenTravel Forum http://www.OpenTravelForum.com

OpenTravel has an extensive discussion Forum to provide an implementation resource for users of its schema, called the OpenTravel Forum, which has all the functionality members expect from a full-featured discussion board, with forums for Architecture, Hospitality, Transport, Travel Services, Tours and Activities, and Implementers Discussion. For employees of OpenTravel member companies, there are several members-only discussion forums that are moderated by individuals who have in-depth experience with OpenTravel schema and their implementation in production environments. Members can post a question and get a response from a moderator within 24 hours (Monday to Friday). Also included are OpenTravel documentation, mailing list subscription, events and announcements, and feedback boards, as well as the OpenTravel Showcase where companies that provide tools, services or technologies to assist in the implementation of OpenTravel schemas can post about their offerings.

- Enhanced OpenTravel Message Codes List Table
The OpenTravel Codes List spreadsheet, included with the specification download, includes a new worksheet named “Index.” This index contains a new, alphabetized, point and click list of all OpenTravel Code List names and 3 character abbreviations to help implementers quickly find code list values.

- Introduction to OpenTravel Webinar
If you are new to the OpenTravel specification, an Introduction to OpenTravel webinar is available at no cost. Please visit the OpenTravel website (http://opentravel.org/News/ArticleView.aspx?ArticleID=59) for a webinar schedule and instructions on how to sign up.

======================================
Other Resources
======================================

Comments may be submitted at any time and members can view the “OpenTravel Specification Comments” page on the OpenTravel wiki at http://wiki.opentravel.org/index.php/Members:OpenTravel_Specification_Comment_Reports to track current and resolved comments.

================
Important Notice
================

As of the 2010A specification publication, OpenTravel no longer includes flattened versions of the OpenTravel messages. Please read the "Creating and Using Flattened OpenTravel Schemas" post on the OpenTravel Forum (http://www.OpenTravelForum.com/) website in the "OpenTravel Documentation" area (http://www.opentravelcommunityforum.com/forum/viewforum.php?f=9) for an overview on flattened schemas and a link to a free schema flattening tool that's available. Please note that OpenTravel does not endorse or provide technical support for any third party tools.

============
Special Note
============

- Excerpts from the W3C XML Schema Primer:

"In an instance document, the attribute xsi:schemaLocation provides hints from the author to a processor regarding the location of schema documents. The author warrants that these schema documents are relevant to checking the validity of the document content, on a namespace by namespace basis."

"The schemaLocation attribute contains pairs of values: The first member of each pair is the namespace for which the second member is the hint describing where to find to an appropriate schema document. The presence of these hints does not require the processor to obtain or use the cited schema documents, and the processor is free to use other schemas obtained by any suitable means, or to use no schema at all."

The intended OpenTravel Schema is listed as the second value in each xsi:schemaLocation in each example instance. This Schema is available as part of the OpenTravel download. Please be aware that your individual processors may treat this declaration in a variety of manners (e.g., an absolute path may be required to obtain a valid parse of the example instances).
