


=============================================
OPENTRAVEL 2016B README
=============================================

=============================
2016B Publication Contents
=============================

- The following documents are included with the OpenTravel 2016B Publication:

----------- OpenTravel_CodeTable (folder) -----------  
- OpenTravel_CodeLists_2016_11_03.zip - A folder containing the OpenTravel Code Table zip file in Microsoft Excel format. The OpenTravel Code List and the OpenTravel Optimized Code List (Phase I) spreadsheets, included with the specification download, includes an alphabetized, point and click list of all OpenTravel Code List names (with 3 character abbreviations) and errors and warnings to help implementers quickly find code list values.

----------- OpenTravel_2016B_XML (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 

----------- OpenTravel_2016B_Schema_Versioning.pdf ----------- 
- OpenTravel began tracking versions in the 2003B release cycle. Prior to the 2008A release, the version table contained 2001 and 2002 data for newly created messages. This document contains a table with each OpenTravel message version from 2006A through 2016B.

----------- OpenTravel_2016B_Comments_Report.pdf ----------- 
- This document contains comments that were entered against the OpenTravel 2016A specification and resulted in changes to the 2016B specification.

----------- OpenTravel_SchemaDesignBestPracticesV3.08.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

----------- OpenTravel_2016B_XMLMessageSuite_ReleaseNotes.pdf ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2016A release and the 2016B release. 

----------- OpenTravel_2016B_Message_Users_Guide.pdf ----------- 
- The Message Users Guide (MUG) contains a description of each OpenTravel Message.  It provides a high-level overview of message functionality. 

----------- OpenTravel_ImplementationGuide_v1.2_ExecSum.pdf -------------
- This is an executive summary of the OpenTravel Implementation Guide. The purpose of the OpenTravel Implementation Guide is to provide invaluable information to both analysts and implementers of the OpenTravel specification on how to more easily understand and build software systems that are interoperable with other travel systems using the OpenTravel schema. The full Guide is available to members of the OpenTravel Alliance via the Wiki http://wiki.opentravel.org/index.php/Public:Resources.

----------- OpenTravel_FastRez (folder) -----------
- OpenTravel_FastRez.zip: A zipped file containing OpenTravel FastRez Schema, WSDL and User Documentation.

----------- OpenTravel_Other (folder) -----------
- OpenTravel Hotel Schema Disability Audit Results: An OpenTravel Hotel Disability Project Brief artifact has been included with the OpenTravel 2011B 1.0 XML Schema Message publication. The OpenTravel Hotel Disability project was focused on a subset of the new 2010 ADA legislation that specifically applies to electronic hotel reservations and includes identifying and describing accessible features; reserving, upon request, accessible guest rooms or specific types of guest rooms and ensuring that the guest rooms requested are blocked and removed from all reservations systems; and guaranteeing the specific accessible guest room. Per the audit results, relatively few changes were made to OpenTravel Hotel schema, with one change made to one common hotel schema (OTA_HotelCommonTypes) to provide a more consistent and structured way to pass measurement information, and annotation changes made to three hotel schema (OTA_HotelCommonTypes, OTA_RailCommonTypes and OTA_RailPreferences) to accommodate renaming the OpenTravel Code List Physically Challenged Feature code table. The slide show included with the publication includes an overview of the project.

=================================================
2016B Significant Schema Updates
=================================================

----Modified Schema----

Common
-- Renamed enumeration: Fuel urcharge to FuelSurcharge in OTA_Lists/List_VehicleChargePurpose_Base to correct typo. 
-- Removed space after the following enumerations in OTA_Lists/List_RatePlanType_Base: "Consortia" and "Weekend" to correct validation error in with some tools.
-- Removed space after the following enumerations in OTA_List/List_ReservationBillingType_Base: "Group" to correct validation error in with some tools.
-- Removed space after the following enumerations in OTA_List/List_VehSize_Base:  "SmallSUV" to correct validation error in with some tools.
-- Added enumeration BusStation to OTA_Lists/List_GroundLocationType_Base.
-- Added enumeration Boat to OTA_Lists/List_VehCategory_Base.
-- Added enumeration Train to OTA_Lists/List_VehCategory_Base.

Ground
-- Changed the type on OTA_GroundAvailRS/GroundServices/Fees from GroundServiceChargesType to GroundFeesType to make the availability message consistent with the booking message.
-- Changed OTA_GroundAvailRS/GroundServices/GroundService/Fees number of occurrences from 0..n to 0..1.
-- Changed name of  OTA_GroundCommonTypes/GroundReservationType/Fee to Fees as this is a container element.
-- Added element OTA_GroundCommonTypes/GroundServiceDetailType/MultimediaDescriptions of type MultimediaDescriptions type with 0..1 occurrences.
-- Added element OTA_GroundCommonTypes/GroundShuttleType/MultimediaDescriptions of type MultimediaDescriptions type with 0..1 occurrences.

======================================================
OpenTravel Implementation Guide Available for Members
======================================================

The OpenTravel Implementation Guide provides information that an implementer of the OpenTravel specification can use to more easily build software systems that are interoperable with other travel systems. The guide also should be useful for analysts who need to understand how to use the OpenTravel specification. The OpenTravel Implementation Guide is available to members through the OpenTravel wiki http://wiki.opentravel.org/index.php/Members:OpenTravel_Implementation_Guide.

======================================
Other Resources
======================================

Comments may be submitted at any time via the comment submission form located at http://www.opentravel.org/Specifications/CommentOnSpec.aspx  

- The OpenTravel Forum http://www.OpenTravelForum.com
OpenTravel has an extensive discussion Forum to provide an implementation resource for users of its schema, called the OpenTravel Forum, which has all the functionality members expect from a full-featured discussion board, with forums for Architecture, Hospitality, Transport, Travel Services, Tours and Activities, and Implementers Discussion. Also included are OpenTravel documentation, mailing list subscription, events and announcements, and feedback boards, as well as the OpenTravel Showcase where companies that provide tools, services or technologies to assist in the implementation of OpenTravel schemas can post about their offerings.

- OpenTravel Message Codes List Table
The OpenTravel Codes List spreadsheet, included with the specification download, includes a worksheet named “Index.” This index contains a new, alphabetized, point and click list of all OpenTravel Code List names and 3 character abbreviations to help implementers quickly find code list values.



