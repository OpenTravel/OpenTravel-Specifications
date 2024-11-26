=============================================
OPENTRAVEL 2011A README
=============================================

=============================
2011A Publication Contents
=============================

- The following documents are included with the OpenTravel 2011A Publication:

----------- OpenTravel_CodeTable (folder) -----------  
- OpenTravel_CodeList_2011_06_15.xls - OpenTravel Code Tables in Microsoft Excel format. The OpenTravel Codes List spreadsheet, included with the specification download, includes an alphabetized, point and click list of all OpenTravel Code List names (with 3 character abbreviations) and errors and warnings to help implementers quickly find code list values. New features for this year’s code list are:

The “index” sheet has been replaced by a <FIND/ SEARCH CODE LISTS> and <FIND/ SEARCH> buttons on the top of the Codelists and Error Codes sheets.

Code Lists
When the search button is clicked, a pop-up window appears with:
-CODE LISTS: A clickable list of all OpenTravel Code Lists. Clicking on a list name will bring you directly to that code list. If you are looking for a specific code list, you can sort the list alphabetically by code list name or code list acronym (by clicking on the SORT BY “Name” and “Code” radio buttons.
-SEARCH FOR: A search feature that allows you to do a filtered key word search as follows:
--Exact Search: Selecting this filter allows you to do an exact match search on your search keywords, e.g. if you want to just find “spa” and not have all code list names and code list values that have the characters “spa” in them (such as “space”), you simply select the “exact search” checkbox.
--Search In: You may select the “Names” and/or “Descriptions” options to include Code List names and descriptions in your search (in addition to code list items.)
-The search returns code list names, values and descriptions that meet your keyword search criteria and search filters. The search results are shown in a search results listbox and you simply click on the item you would like to go to.

Errors & Warnings
When the search button is clicked, a pop-up window appears with:
-SEARCH/FIND: A search feature that allows you to do a key word search
-The search returns error and warning descriptions that meet your keyword search criteria. The search results are shown in a search results listbox and you simply click on the item you would like to go to.

----------- OpenTravel2011A_XML (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 
- XML Instance files- Example XML instance documents in individual files that are taken directly from the use cases in the OpenTravel_MessageUserGuide_2011A.pdf.

----------- 2011A_Schema_Versioning.pdf ----------- 
- OpenTravel began tracking versions in the 2003B release cycle. Prior to the 2008A release, the version table contained 2001 and 2002 data for newly created messages. This document contains a table with each OpenTravel message version from 2006A through 2011A.

----------- 2011A_Comments_Report.pdf ----------- 
- This document contains comments that were entered against the OpenTravel 2010B specification and resulted in changes to the 2011A specification.

----------- OpenTravel_SchemaDesignBestPracticesV3.08.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

----------- OpenTravel_ReleaseNotes_2011A.pdf ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2010B release and the 2011A release. 

----------- OpenTravel_MessageUserGuide_2011A.pdf ----------- 
- The Message Users Guide (MUG) contains a description of each OpenTravel Message with sample use cases and links to XML instance documents. It provides a high-level overview of message functionality and includes:
	-A point-and-click index of business functionality and use cases for each message, allowing an implementer to quickly identify the OpenTravel messages that suit their own and their trading partner business requirements,
	-Links to each message (summarized) data dictionary that allow implementers to see the names and descriptions of elements and attributes in a message and the enumeration values where applicable,
	-Extended message scenario use cases that help implementers understand the range of business scenarios that can be accomplished per message,
	-An “Introduction and Getting Started” section that includes links to OpenTravel implementer/member resources, OpenTravel schema architecture basics, and links to all third party standards referenced in OpenTravel messages to help implementers understand the relationships between OpenTravel messages and other third party standards, and,
	-Point-and-click access to online message sample use case instances that allow an implementer to access only the sample instances they require (note that these instances were not intended for production use by implementers, but rather for human reference.)

----------- OpenTravel_ImplementationGuide_v1.2_ExecSum.pdf -------------
- This is an executive summary of the OpenTravel Implementation Guide. The purpose of the OpenTravel Implementation Guide is to provide invaluable information to both analysts and implementers of the OpenTravel specification on how to more easily understand and build software systems that are interoperable with other travel systems using the OpenTravel schema. The full Guide is available to members of the OpenTravel Alliance via the Wiki http://wiki.opentravel.org/index.php/Public:Resources.

----------- OpenTravel_FastRez (folder) -----------
- OpenTravel_FastRez.zip: A zipped file containing OpenTravel FastRez Schema, WSDL and User Documentation.

=========================================
2011A New Schemas and Significant Schema Updates
=========================================

- OTA_HotelCacheChangeNotifRQ/RS.xsd: The OpenTravel Hotel Cache Change Notification message set allows a hotel supplier to push their changed hotel rates and availability information to a trading partner that caches their hotel rates and availability information and have the trading partner send an acknowledgement message that they received the information.

- OTA_Ground Transportation Messages: The new OpenTravel Ground Transportation schema is designed to support XML distribution for the personal ground transportation sector (that includes limousine, black car and personal shuttle service) and covers the scope of web services required to implement a modern personal ground transportation reservation system. The 2011A OpenTravel Publication includes three new Ground Transportation message sets:
  • OTA_GroundAvailRQ/RS – Check ground transfer service availability
  • OTA_GroundBookRQ/RS – Create a ground transportation service reservation (booking)
  • OTA_GroundResRetrieveRS/RS – Retrieve a ground transportation service reservation

- Enhanced, deprecated and new OpenTravel Rail messages
  • One deprecated rail message (OTA_RailRetrieveRS)
  • Three enhanced 2010B message sets (OTA_RailAvailRQ/RS, OTA_RailBookRQ/RS, OTA_RailScheduleRQ/RS)
  • Five new rail messages (OTA_RailReadRQ, OTA_RailResRetrieveSummaryRS, OTA_RailResRetrieveDetailRS, OTA_RailPriceRQ/RS, OTA_RailFareQuoteRQ/RS)

- Billing Instruction Details in Hotel Messages: OpenTravel is pleased to announce support for billing instruction details in OpenTravel Hotel schema. This new functionality allow hotels to create billing codes that apply to a set of instructions for a transaction set that are routed to a designated folio.
  Enhanced hotel messages are:
  • OTA_HotelReservation
  • OTA_HotelResNotifRQ
  • OTA_HotelResModifyRQ
  • OTA_HotelResRQ
  • OTA_HotelResRS

- Hostel Support in Hotel Messages: OpenTravel is pleased to announce support for Hosteliers in the OpenTravel Hotel messages. New attributes and elements are provided for room (occupancy) gender assignment, shared rooms, availability results sort order and bedding configurations that are unique to Hostels.
  Enhanced hotel messages are:
  • OTA_HotelCommonTypes
  • OTA_HotelAvailRQ/RS
  • OTA_HotelAvailNotifRQ
  • OTA_HotelResRQ/RS

- Rebate Program Information in Hotel Messages: OpenTravel is pleased to announce support for suppliers participating in rebate programs. The 2011A implementation focuses on hotel suppliers and includes enhancements to OpenTravel Hotel Search, Hotel Availability and Hotel Get Availability messages that allow hotel suppliers to let their customers search for hotels by participation in rebate programs, and display their rebate program participation information in availability messages. This first implementation is modeled after a Value Added Tax  rebate program, but the implementation is flexible enough to support other rebate programs that suppliers may offer or participate in. The following OpenTravel common and Hotel messages have been enhanced to include the exchange of rebate program information: 
  • OTA_CommonTypes
  • OTA_HotelSearchRQ/RS
  • OTA_HotelAvailGetRQ
  • OTA_HotelAvailRQ/RS

======================================================
OpenTravel Implementation Guide Available for Members
======================================================

The OpenTravel Implementation Guide provides information that an implementer of the OpenTravel specification can use to more easily build software systems that are interoperable with other travel systems. The guide also should be useful for analysts who need to understand how to use the OpenTravel specification. The OpenTravel Implementation Guide is available to members through the OpenTravel wiki http://wiki.opentravel.org/index.php/Members:OpenTravel_Implementation_Guide.

======================================
Other Resources
======================================

Comments may be submitted at any time and members can view the “OpenTravel Specification Comments” page on the OpenTravel wiki at http://wiki.opentravel.org/index.php/Members:OpenTravel_Specification_Comment_Reports to track current and resolved comments.

- The OpenTravel Forum http://www.OpenTravelForum.com
OpenTravel has an extensive discussion Forum to provide an implementation resource for users of its schema, called the OpenTravel Forum, which has all the functionality members expect from a full-featured discussion board, with forums for Architecture, Hospitality, Transport, Travel Services, Tours and Activities, and Implementers Discussion. Also included are OpenTravel documentation, mailing list subscription, events and announcements, and feedback boards, as well as the OpenTravel Showcase where companies that provide tools, services or technologies to assist in the implementation of OpenTravel schemas can post about their offerings.

- OpenTravel Data Dictionaries 
OpenTravel is pleased to announce new schema data dictionaries, which provide accurate and up to date structured references of OpenTravel schema. Data dictionary documentation is provided for all aspects of each schema file, including Elements, Simple Types, Complex Types, Groups, Attributes, Attribute Groups, Constraints and Facets. Additional documentation includes overview tables that illustrate child structures below elements, complex types and attribute groups and documentation of Global Attributes, Groups, key, keyref and unique constraints. The list of OpenTravel Data Dictionaries may be found on the OpenTravel Data Dictionaries page on the OpenTravel wiki at http://wiki.opentravel.org/index.php/Public:OpenTravel_Data_Dictionaries. NOTE: 2011A Schema Dictionaries will be available with the June OpenTravel Publication.

- OpenTravel Message Codes List Table
The OpenTravel Codes List spreadsheet, included with the specification download, includes a worksheet named “Index.” This index contains a new, alphabetized, point and click list of all OpenTravel Code List names and 3 character abbreviations to help implementers quickly find code list values.

- Introduction to OpenTravel Webinar
If you are new to the OpenTravel specification, an Introduction to OpenTravel webinar is available at no cost. Please visit the OpenTravel website (http://opentravel.org/News/ArticleView.aspx?ArticleID=59) for a webinar schedule and instructions on how to sign up.

================
Important Notice(s)
================

- The OpenTravel OTA_RailRetrieveRS message has been deprecated from OpenTravel schema. In its place, implementers are encouraged to use one or both of the new Rail Reservation Read messages (OTA_RailResRetrieveSummary.xsd and OTA_RailResRetrieveDetails.xsd). Note that the OTA_RailReadRQ (Rail Reservation Read request) message contains a root level attribute named ResInfoLevel, which is an enumerated attribute with two choices: 1) Summary, and 2) Detail. This attribute is an indicator of whether summary or detailed reservation information should be returned in a Rail Reservation Read response message.

- The OpenTravel OTA_HotelInvChangeRQ/RS messages have been renamed to OTA_HotelCacheChangeRQ/RS respectively. This name change was done to align the full suite of OpenTravel Hotel Cache messages, including the new 2011A OTA_HotelCacheChangeNotifRQ/RS message set.

- Some 2011A OpenTravel Schema are non-backwards compatible (due to project team and workgroup enhancements):
  • OTA_RailPreferences.xsd
  • OTA_RailCommonTypes.xsd
  • OTA_AirCommonTypes.xsd

- OpenTravel Public review schema namespaces have been changed to http://www.opentravel.org/OTA/2003/05/beta
