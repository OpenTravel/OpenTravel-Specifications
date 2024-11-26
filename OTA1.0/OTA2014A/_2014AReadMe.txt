


=============================================
OPENTRAVEL 2014A README
=============================================

=============================
2014A Publication Contents
=============================

- The following documents are included with the OpenTravel 2014A Publication:

----------- OpenTravel_CodeTable (folder) -----------  
- A folder containing the OpenTravel_CodeList_2014_06_06.zip file in Microsoft Excel format. The OpenTravel Codes List spreadsheet, included with the specification download, includes an alphabetized, point and click list of all OpenTravel Code List names (with 3 character abbreviations) and errors and warnings to help implementers quickly find code list values.

----------- OpenTravel_2014A_XML (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 

----------- OpenTravel_2014A_Schema_Versioning.pdf ----------- 
- OpenTravel began tracking versions in the 2003B release cycle. Prior to the 2008A release, the version table contained 2001 and 2002 data for newly created messages. This document contains a table with each OpenTravel message version from 2006A through 2014A.

----------- OpenTravel_2014A_Comments_Report.pdf ----------- 
- This document contains comments that were entered against the OpenTravel 2013B specification and resulted in changes to the 2014A specification.

----------- OpenTravel_SchemaDesignBestPracticesV3.08.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

----------- OpenTravel_2014A_XMLMessageSuite_ReleaseNotes.pdf ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2013B release and the 2014A release. 

----------- OpenTravel_2014A_Message_Users_Guide.zip ----------- 
- The Message Users Guide (MUG) contains a description of each OpenTravel Message.  It provides a high-level overview of message functionality. 

----------- OpenTravel_ImplementationGuide_v1.2_ExecSum.pdf -------------
- This is an executive summary of the OpenTravel Implementation Guide. The purpose of the OpenTravel Implementation Guide is to provide invaluable information to both analysts and implementers of the OpenTravel specification on how to more easily understand and build software systems that are interoperable with other travel systems using the OpenTravel schema. The full Guide is available to members of the OpenTravel Alliance via the Wiki http://wiki.opentravel.org/index.php/Public:Resources.

----------- OpenTravel_FastRez (folder) -----------
- A folder containing the OpenTravel_FastRez.zip file. This is zipped file containing OpenTravel FastRez Schema, WSDL and User Documentation.

----------- OpenTravel_Other (folder) -----------
- OpenTravel Hotel Schema Disability Audit Results: An OpenTravel Hotel Disability Project Brief artifact has been included with the OpenTravel 2011B 1.0 XML Schema Message publication. The OpenTravel Hotel Disability project was focused on a subset of the new 2010 ADA legislation that specifically applies to electronic hotel reservations and includes identifying and describing accessible features; reserving, upon request, accessible guest rooms or specific types of guest rooms and ensuring that the guest rooms requested are blocked and removed from all reservations systems; and guaranteeing the specific accessible guest room. Per the audit results, relatively few changes were made to OpenTravel Hotel schema, with one change made to one common hotel schema (OTA_HotelCommonTypes) to provide a more consistent and structured way to pass measurement information, and annotation changes made to three hotel schema (OTA_HotelCommonTypes, OTA_RailCommonTypes and OTA_RailPreferences) to accommodate renaming the OpenTravel Code List Physically Challenged Feature code table. The slide show included with the publication includes an overview of the project.

================================================
2014A Significant Schema Updates
================================================

----Modified Schema----


Common
- Added a new optional element Warning of type WarningType to OTA_CommonTypes/EncryptionTokenType to allow for the reporting of individual errors within payment information.
- Added a new enumeration of Transportation to OTA_Lists/List_QuestionCategory to allow for the identification of transportation options.
- Added a new optional attribute SequenceNbr of type xs:nonNegativeInteger to OTA_CommonTypes/TaxType to allow for the ordering of taxes when displayed within booking rules.
- Added a new optional attribute Duration of type DurationType to OTA_CommonTypes/TaxType to allow for the duration for which the tax applies to be indicated.
- Added a new optional attribute Name of type StringLength1to64 to OTA_CommonTypes/SourceType/RequestorID to allow for the name of the booking party to be indicated.

Hotel
- Added an new optional attribute MaxCribs of type xs:nonNegativeInteger to OTA_HotelCommonTypes/GuestRoomType/Quantities to allow for the indication of the number of cribs allowed in a room type.

Insurance 
- Added new optional element Orgin with an optional child element CountryName of type CountryNameType was added to OTA_InsuranceCommonTypes/TripFeaturesType to allow for the inclusion of the orgin country.

Reviews
- Added a new optional attribute MainQuestionInd of type xs:boolean to OTA_Reviews/Questions/QuestionCategory/Question to identify the main question within a category.

Air
- Removed text &nbsp at the beginning of the OTA_AirAvailRQ message that was added in error to allow for the schema to validate.

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



