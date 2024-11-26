=============================================
OPENTRAVEL 2010B README
=============================================

=============================
2010B Publication Contents
=============================

- The following documents are included with the OpenTravel 2010B Publication:

----------- OpenTravel_CodeTable (folder) -----------  
- OpenTravel_CodeList_2010_12_2.xls- OpenTravel Code Tables in Microsoft Excel format. 
- OpenTravel_CodeTable2010_12_2.xml- OpenTravel Code Tables in XML format. 
- OpenTravel_CodeTable.xsd- OpenTravel XML Schema that are used to validate the OpenTravel Code Tables in XML format.

----------- OpenTravel2010B_XML (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 
- XML Instance files- Example XML instance documents in individual files that are taken directly from the use cases in the OpenTravel_MessageUserGuide_2010B.pdf.

----------- OpenTravel_MessageUsersGuide_2010B.pdf ----------- 
- The Message Users Guide (MUG) contains a description of each OpenTravel Message with sample use cases and links to XML instance documents. It provides a high-level overview of message functionality and includes:
	-A point-and-click index of business functionality and use cases for each message, allowing an implementer to quickly identify the OpenTravel messages that suit their own and their trading partner business requirements,
	-Links to each message (summarized) data dictionary that allow implementers to see the names and descriptions of elements and attributes in a message and the enumeration values where applicable,
	-Extended message scenario use cases that help implementers understand the range of business scenarios that can be accomplished per message,
	-An “Introduction and Getting Started” section that includes links to OpenTravel implementer/member resources, OpenTravel schema architecture basics, and links to all third party standards referenced in OpenTravel messages to help implementers understand the relationships between OpenTravel messages and other third party standards, and,
	-Point-and-click access to online message sample use case instances that allow an implementer to access only the sample instances they require (note that these instances were not intended for production use by implementers, but rather for human reference.)

----------- OpenTravel_MessageXSDVersioningTable_2010B.pdf ----------- 
- OpenTravel began tracking versions in the 2003B release cycle. Prior to the 2008A release, the version table contained 2001 and 2002 data for newly created messages. This document contains a table with each OpenTravel message version from 2003B through 2010A. This document may also be found on the OpenTravel wiki in the "Implementation" section on the main page (http://wiki.opentravel.org/index.php/Main_Page).

----------- OpenTravel_SchemaDesignBestPracticesV3.08.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

----------- OpenTravel_ReleaseNotes_2010B.pdf ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2010A release and the 2010B release. 

----------- OpenTravel_ImplementationGuide_v1.2_ExecSum.pdf --------------
- This is an executive summary of the OpenTravel Implementation Guide. The purpose of the OpenTravel Implementation Guide is to provide invaluable information to both analysts and implementers of the OpenTravel specification on how to more easily understand and build software systems that are interoperable with other travel systems using the OpenTravel schema. The full Guide is available to members of the OpenTravel Alliance via the Wiki http://wiki.opentravel.org/index.php/Public:Resources.

----------- OpenTravel_FastRez (folder) -----------
- OpenTravel_FastRez.zip: A zipped file containing OpenTravel FastRez Schema, WSDL and User Documentation. See “Important Notices” below for an overview of FastRez.

=========================================
2010B New Schemas and Significant Schema Updates
=========================================

- OTA_HotelInvChangeRQ/RS.xsd: The OpenTravel Hotel Inventory Change message pair facilitates streamlined hotel inventory availability transactions for trading partners that cache hotel rates and availability information from hotel suppliers. The messages are designed to alleviate two significant challenges faced by both hotel suppliers and their trading partners, which are out of synch caches and rising infrastructure/support costs associated with handling a high volume of availability transactions.

- OTA_RailScheduleRQ/RS.xsd: The OpenTravel Rail Schedule message pair facilitates exchanging rail schedule information between a rail supplier and trading partners. The Rail Schedule message pair is typically used as a precursor to Rail Availability (OTA_RailAvailRQ/RS) messages and may be used to reduce transaction load against a rail rates and availability system when inventory availability and fares are not required.

- OTA_RailConfirmBookingRQ/RS.xsd: The 2010B enhanced Rail booking messages support both transactional queued and non-transactional queued provisional booking message implementations. Note that a “provisional” booking is a reservation that may have been processed successfully using the OTA_RailBookRQ message, but has not been confirmed in the trading partners system as committed or cancelled. The Rail Confirm Booking message pair confirms one or more provisionally booked messages.

- OTA_RailIgnoreBookingRQ/RS.xsd: The 2010B enhanced Rail booking messages support both transactional queued and non-transactional queued provisional booking message implementations. Note that a “provisional” booking is a reservation that may have been processed successfully using the OTA_RailBookRQ message, but has not been confirmed in the trading partners system as committed or cancelled. The Rail Ignore Booking message pair cancels one or more provisionally booked messages.

- OTA_RailPaymentRQ/RS.xsd: The Rail Payment message pair is used to submit a payment for a rail reservation. This message is typically used in some combination with the OTA_RailBookRQ/RS, OTA_RailConfirmBookingRQ/RS and OTA_RailIgnoreBookingRQ/RS messages.

- Vehicle Rental No Show Fees in Car Messages: For the vehicle rental industry, the new OpenTravel “Vehicle Rental No Show Fee” functionality facilitates the efficient utilization of a smaller fleet while providing transparency of no show fee policies and other information for maintaining a high level of customer satisfaction. In addition to the existing functionality in OpenTravel car schema that addresses charging cancellation fees when a reservation is actually cancelled, the new “Vehicle Rental No Show Fee” functionality facilitates a no show fee charged to a customer that books a reservation, does not cancel it, and then fails to pick up the vehicle. The vehicle no show fee is specified at the individual vehicle level, e.g. there is no method to specify that a no show fee applies to all vehicles returned in a Vehicle Availability & Rates or Vehicle Rate Rule response message. Two key concepts within the no show fee functionality are deadlines and grace periods. A deadline specifies the vehicle rental company’s policy about the time by which a reservation cancellation must be made to avoid the no show fee. The grace period represents the time period between a scheduled pick-up time and when the no show fee is invoked.

- Electronic Miscellaneous Documents (EMD) for Air Messages: Electronic miscellaneous document (EMD) business functionality in OpenTravel air messages allows OpenTravel implementers to exchange fee-related information (that is separate from a fare) for items and services passengers can purchase to enhance their travel experience. These items and services include inflight amenities such as meals and entertainment and the sale of merchandise. Additionally, other EMD fees, such as fees for baggage charges may be exchanged. EMD’s are stored in a reservation system (in conjunction with a booking transaction) if there is any relationship to a PNR (passenger name record) and are stored in ticketing segments if there is any association to an eTicket.

- Charitable Donation Information in Air, Car and Hotel Booking Request Messages: OpenTravel is pleased to announce support for micro-donations in OpenTravel Air, Car and Hotel booking request messages. The current implementation supports “Massive Good” micro-donations but is flexible in its support for any type of micro-donation in an OpenTravel booking request message due to the reuse of OpenTravel elements, simple types and attribute groups.

======================================================
OpenTravel Implementation Guide Available for Members
======================================================

The OpenTravel Implementation Guide provides information that an implementer of the OpenTravel specification can use to more easily build software systems that are interoperable with other travel systems. The guide also should be useful for analysts who need to understand how to use the OpenTravel specification. The OpenTravel Implementation Guide is available to members through the OpenTravel wiki http://wiki.opentravel.org/index.php/Members:OpenTravel_Implementation_Guide.

======================
New Resource Available
======================

- OpenTravel Data Dictionaries 
OpenTravel is pleased to announce new schema data dictionaries, which provide accurate and up to date structured references of OpenTravel schema. Data dictionary documentation is provided for all aspects of each schema file, including Elements, Simple Types, Complex Types, Groups, Attributes, Attribute Groups, Constraints and Facets. Additional documentation includes overview tables that illustrate child structures below elements, complex types and attribute groups and documentation of Global Attributes, Groups, key, keyref and unique constraints. The list of OpenTravel Data Dictionaries may be found on the OpenTravel Data Dictionaries page on the OpenTravel wiki at http://wiki.opentravel.org/index.php/Public:OpenTravel_Data_Dictionaries.

======================================
Other Resources
======================================

Comments may be submitted at any time and members can view the “OpenTravel Specification Comments” page on the OpenTravel wiki at http://wiki.opentravel.org/index.php/Members:OpenTravel_Specification_Comment_Reports to track current and resolved comments.

- The OpenTravel Forum http://www.OpenTravelForum.com
OpenTravel has an extensive discussion Forum to provide an implementation resource for users of its schema, called the OpenTravel Forum, which has all the functionality members expect from a full-featured discussion board, with forums for Architecture, Hospitality, Transport, Travel Services, Tours and Activities, and Implementers Discussion. Also included are OpenTravel documentation, mailing list subscription, events and announcements, and feedback boards, as well as the OpenTravel Showcase where companies that provide tools, services or technologies to assist in the implementation of OpenTravel schemas can post about their offerings.

- OpenTravel Message Codes List Table
The OpenTravel Codes List spreadsheet, included with the specification download, includes a worksheet named “Index.” This index contains a new, alphabetized, point and click list of all OpenTravel Code List names and 3 character abbreviations to help implementers quickly find code list values.

- Introduction to OpenTravel Webinar
If you are new to the OpenTravel specification, an Introduction to OpenTravel webinar is available at no cost. Please visit the OpenTravel website (http://opentravel.org/News/ArticleView.aspx?ArticleID=59) for a webinar schedule and instructions on how to sign up.

================
Important Notice
================

- OpenTravel Brand Category Code (BCC) Code List has been Deprecated
The OpenTravel Brand Category Code (BCC) that was marked for deletion has been deprecated from the OpenTravel Code List. The OpenTravel Segment Category Code (SEG) table should be used instead.

- FastRez Schema and WSDL Included in 2010B Specification
OpenTravel FastRez is a tightly defined specification for the hotel industry, covering a set of common business functions for electronic distribution. FastRez provides an alternative for emerging or smaller companies who need a quick and easy solution for distributing their travel and traveler information, but may also be useful for larger companies who would like to reduce the cost of connecting with multiple smaller partners. Implementing FastRez in the manner in which it was designed allows a company to seamlessly interoperate with anyone else who also implements the specification. FastRez includes messages to handle the availability, reservation booking, reservation retrieval, and reservation cancellation functions for hotel properties. Each schema is a smaller, more defined version of the 2008B OpenTravel message. The significant reduction in the size of the schemas makes the messages easier and quicker to implement.
