


=============================================
OPENTRAVEL 2013A README
=============================================

=============================
2013A Publication Contents
=============================

- The following documents are included with the OpenTravel 2013A Publication:

----------- OpenTravel_CodeTable (folder) -----------  
- OpenTravel_CodeList_2013_6_17.zip - A zip file containing the OpenTravel Code Table in Microsoft Excel format. The OpenTravel Codes List spreadsheet, included with the specification download, includes an alphabetized, point and click list of all OpenTravel Code List names (with 3 character abbreviations) and errors and warnings to help implementers quickly find code list values.

----------- OpenTravel_2013A_XML (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 

----------- OpenTravel_2013A_Schema_Versioning.pdf ----------- 
- OpenTravel began tracking versions in the 2003B release cycle. Prior to the 2008A release, the version table contained 2001 and 2002 data for newly created messages. This document contains a table with each OpenTravel message version from 2006A through 2013A.

----------- OpenTravel_2013A_Comments_Report.pdf ----------- 
- This document contains comments that were entered against the OpenTravel 2012A specification and resulted in changes to the 2012B specification.

----------- OpenTravel_SchemaDesignBestPracticesV3.08.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

----------- OpenTravel_2013A_XMLMessageSuite_ReleaseNotes.pdf ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2011B release and the 2012A release. 

----------- OpenTravel_ImplementationGuide_v1.2_ExecSum.pdf -------------
- This is an executive summary of the OpenTravel Implementation Guide. The purpose of the OpenTravel Implementation Guide is to provide invaluable information to both analysts and implementers of the OpenTravel specification on how to more easily understand and build software systems that are interoperable with other travel systems using the OpenTravel schema. The full Guide is available to members of the OpenTravel Alliance via the Wiki http://wiki.opentravel.org/index.php/Public:Resources.

----------- OpenTravel_FastRez (folder) -----------
- OpenTravel_FastRez.zip: A zipped file containing OpenTravel FastRez Schema, WSDL and User Documentation.

----------- OpenTravel_Other (folder) -----------
- OpenTravel Hotel Schema Disability Audit Results: An OpenTravel Hotel Disability Project Brief artifact has been included with the OpenTravel 2011B 1.0 XML Schema Message publication. The OpenTravel Hotel Disability project was focused on a subset of the new 2010 ADA legislation that specifically applies to electronic hotel reservations and includes identifying and describing accessible features; reserving, upon request, accessible guest rooms or specific types of guest rooms and ensuring that the guest rooms requested are blocked and removed from all reservations systems; and guaranteeing the specific accessible guest room. Per the audit results, relatively few changes were made to OpenTravel Hotel schema, with one change made to one common hotel schema (OTA_HotelCommonTypes) to provide a more consistent and structured way to pass measurement information, and annotation changes made to three hotel schema (OTA_HotelCommonTypes, OTA_RailCommonTypes and OTA_RailPreferences) to accommodate renaming the OpenTravel Code List Physically Challenged Feature code table. The slide show included with the publication includes an overview of the project.

----------- OpenTravel_2013A_Message_Users_Guide.zip ----------- 
- The Message Users Guide (MUG) contains a description of each OpenTravel Message. It provides a high-level overview of message functionality.
	

================================================
2013A New Schemas and Significant Schema Updates
================================================

----New Schema----

==Common==

The Reviewer Information Project Team created two new OpenTravel 2013A 1.0 XML Schema message pairs.  The focus of this project team was to create messaging to allow the transfer of Reviews that were completed by guests after they used a product or service.  The OTA_ReviewsRQ/RS message set is a pull message to request reviews for specified criteria with the ability to filter the response.  The OTA_ReviewsNotifRQ/RS message set is a push message used to send reviews for specified criteria.
-Both of these new messages were created with the intent to be used by hotels, but written in a generic format so that they can be used by other travel sectors with just minor modifications.

----Modified Schema----

Air
- OTA_AirPriceRS message has been modified to include information concerning an airline private fare.
- The attributes StartingRow and EndingRow's type has been changed from a Numeric1to3 to a NumericStringLength1to3 to allow for up to 3 digit row numbers to be sent.

Hotel
- The BasicPropertyInfoType was added to OTA_HotelReservation at the ResGlobalInfo level to support reservations that are made for services only with no room booking.
- RoomTypeAllocation in OTA_HotelCommonTypes was modified to include a new element and 2 new attributes to allow for the exchange of room type allocation data including occupancy levels.
- Added the RatePlanInclusions element to the HOtelRatePlanType to provide the ability to indicate whether or not Tax is included.
- Added a new attribute MinOccupancy to OTA_HotelContentDescription/HotelDescriptiveContentType/FacilityInfoType/GuestRooms/GuestRoom @MinOccupancy to provide the ability to indicate if a minimum occupancy applies to a room type.
- Added a new attribute RoomStayGroupID of type StringLength1to32 to OTA_HotelAvailRS/RoomStays/RoomStay to pass an ID for a group of rooms which must be booked together.

 

Car
- The PaymentFormType was updated to include a BillingAccountName and BillingAccountAddress to identify billing contact information associated to a voucher.
- Added a new attribute AssocTerminalList of type ListOfStringLength1to32 to provide the ability to specify a terminal(s) within an airport to identify where a car rental counter is located.

Common
- A new enumeration was added to the PaymentCardCodeType of UP to allow for the indication of payment by China UnionPay.
- The POS (Point of Sale) element was added to the OTA_ProfileCreateRQ and OTA_ProfileMergeRQ messages
- Added a new attribute to the OTA_ProfileReadRS message to specify if the Group Days Apply Value can be used for a Voucher Billing Account.  


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

- OpenTravel Message Codes List Table
The OpenTravel Codes List spreadsheet, included with the specification download, includes a worksheet named “Index.” This index contains a new, alphabetized, point and click list of all OpenTravel Code List names and 3 character abbreviations to help implementers quickly find code list values.

- Introduction to OpenTravel Webinar
If you are new to the OpenTravel specification, an Introduction to OpenTravel webinar is available at no cost. Please visit the OpenTravel website for a webinar schedule and instructions on how to sign up.




