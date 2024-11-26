=============================================
OPENTRAVEL 2011B README
=============================================

=============================
2011B Publication Contents
=============================

- The following documents are included with the OpenTravel 2011B Publication:

----------- OpenTravel_CodeTable (folder) -----------  
- OpenTravel_CodeList_2011_11_09.zip - A zip file containing the OpenTravel Code Table in Microsoft Excel format. The OpenTravel Codes List spreadsheet, included with the specification download, includes an alphabetized, point and click list of all OpenTravel Code List names (with 3 character abbreviations) and errors and warnings to help implementers quickly find code list values.

----------- OpenTravel2011B_XML (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 
- XML Instance files- Example XML instance documents in individual files that are taken directly from the use cases in the OpenTravel_MessageUserGuide_2011B.pdf.

----------- OpenTravel_2011B_Schema_Versioning.pdf ----------- 
- OpenTravel began tracking versions in the 2003B release cycle. Prior to the 2008A release, the version table contained 2001 and 2002 data for newly created messages. This document contains a table with each OpenTravel message version from 2006A through 2011B.

----------- OpenTravel_2011B_Comments_Report.pdf ----------- 
- This document contains comments that were entered against the OpenTravel 2011A specification and resulted in changes to the 2011B specification.

----------- OpenTravel_SchemaDesignBestPracticesV3.08.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

----------- OpenTravel_ReleaseNotes _2011B ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2011A release and the 2011B release. 

----------- OpenTravel_MessageUserGuide_2011B.zip ----------- 
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

----------- OpenTravel_Other (folder) -----------
- OpenTravel Hotel Schema Disability Audit Results: An OpenTravel Hotel Disability Project Brief artifact has been included with the OpenTravel 2011B 1.0 XML Schema Message publication. The OpenTravel Hotel Disability project was focused on a subset of the new 2010 ADA legislation that specifically applies to electronic hotel reservations and includes identifying and describing accessible features; reserving, upon request, accessible guest rooms or specific types of guest rooms and ensuring that the guest rooms requested are blocked and removed from all reservations systems; and guaranteeing the specific accessible guest room. Per the audit results, relatively few changes were made to OpenTravel Hotel schema, with one change made to one common hotel schema (OTA_HotelCommonTypes) to provide a more consistent and structured way to pass measurement information, and annotation changes made to three hotel schema (OTA_HotelCommonTypes, OTA_RailCommonTypes and OTA_RailPreferences) to accommodate renaming the OpenTravel Code List Physically Challenged Feature code table. The slide show included with the publication includes an overview of the project.

=========================================
2011B New Schemas and Significant Schema Updates
=========================================

----New Schema----

Air

The OpenTravel air merchandising project team created one new OpenTravel 2011B 1.0 XML Schema message pair and one supporting (air) vertical common types file. The focus of this project team was to provide OpenTravel schema functionality to address the emerging airline sector ancillary revenue (merchandising), as airlines worldwide are expected to generate over $58 billion USD in ancillaries in 2010 alone. The new message pair, OTA_AirGetOfferRQ/RS, includes the following functionality:

The Get Offer request message provides trip and passenger characteristics to be used by an offer processing system to target relevant offers. Request criteria may be specified for the entire trip or by individual traveler and/or arranger and include any combination of the following:
• Confirmed booking —including air itinerary, traveler/arranger, purchased offers, payment, pricing and ticketing information
• Pre-booking —including origin/destination, itinerary, traveler/arranger preferences and specific flight information
• Baggage —including item type, quantity, description, origin/destination, marketing/operating carriers and traveler/itinerary association
• Seat information —including marketing classification, requested quantity and traveler/itinerary association
• Offers to include and/or exclude
• Offers that have already been presented and/or purchased

Additional supported business functionality includes:
• Offer family encoding by airline suppliers and/or ATPCO
• Detailed point of sale information
• Pricing structure flexibility, including display/ pricing currency(s), ticketing country/ city, and loyalty program redemption support
• Offer stages that specify the stage in the journey at which the ancillary offer request is being made or the offer was purchased, e.g. shopping and check-in
• Travel insurance product offers included with ancillary offers

The new Get Offer response message returns relevant offers that meet the search criteria. Returned information includes:
• Pricing structure details—including exchange rates, currency overrides and accepted payment currency that apply to all offers unless override information is provided elsewhere in the message
• Priced offers—Priced offer information, including offer name and description, maximum and minimum offer quantity(s), service family, pricing details including redemption mile pricing, booking instructions, restrictions, penalties, multimedia, commissions and currency overrides

Ground

The OpenTravel ground transportation project team created two new message pairs and a new modify booking message (note that the modify booking has the existing OTA_GroundBookRS as the response message.) 
• The OTA_GroundCancelRQ/RS message pair requests the cancellation of one confirmed ground reservation and responds with cancellation confirmation information.
• The OTA_GroundModifyRQ message requests the modification of an existing reservation (booking) request message, and includes the information required to change the reservation. Note that the response for this modification is the OTA_GroundBookRS message.

• The OTA_GroundResNotifRQ/RS message pair is designed to be used as an unsolicited push notification message between IT systems and/or trading partners. This message includes the information required to create or store details for one ground transportation reservation that may have multiple segments associated with it.

Rail

The OpenTravel rail schema project team created one new OpenTravel 2011B 1.0 XML Schema message pair and made enhancements to the (common) OTA_Profile.xsd schema to support enhanced rail (customer) preference information. The new message pair, OTA_RailShopRQ/RS, specifies search criteria for which rail pricing and availability should be searched for and includes the following functionality:
Search criteria may include:
• Information about the outbound (and optional return and connecting locations) between which availability and low fares available are to be checked
• Passenger type(s) and category(s)
• Global preferences for all origin and destination locations for both outbound and return trips (note that these preferences may be overridden elsewhere in the message) and include rail operator, transport modes, accommodations and amenities
• Specific train number/ network code combination or just a network code
• Rate qualifier(s) to specify the type of fares of interest to the traveler, along with any discount number or promotional codes that may affect the fare
• Fare basis code(s) that apply to the whole trip

Additional message functionality includes specifying detail point of sale information for the message initiator.

The Rail Shop response message contains pricing and availability details for the requested search criteria, including origin/ destination location, accommodations and departure/ return dates and times. For each specified O/D pair, train options may be specified that include:
• Origin/Destination location code and optional code context
• Journey segment availability detail information, which may be for a train or a bus segment, and includes:
• Specific inventory-controlled service class code or detailed accommodation information
• Class and passenger type fares
• Other service-related information including reservation class, reservation type, different class codes and auto train vehicle type

Pricing details may be specified at the origin/ destination pair and/ or segment level, and include basic fare, alternate currency with exchange rate details, terms and conditions, adjustments, discounts, fees, taxes and ancillary charges.

----Significantly Enhanced Schema----

Day Tours & Activities

The 2011A Tours schema messages (OTA_Tours) have been renamed and enhanced (for the 2011B OpenTravel Publication) to support both day tours and activities. This enhancement was made due to the data and booking path transactional similarity between day tour and activity travel segments. The new root level prefix of the 1.0 XML Messages is OTA_TourActivity. Enhanced functionality includes:
• Support for commissions, additional (and structured) categories & types, associated lodging information, detailed policy definitions, supplier and operator definitions, extra amenity definitions and pricing enhancements for promotions and negotiated rates.
• 4 new messages (in addition to enhanced search and availability messages) to provide full booking path functionality: Booking, Booking Modification, Booking Cancel and Reservation Retrieve.
• 1 deprecated notification message pair (OTA_TourInformationNotifRQ/RS) that will be recreated as part of a 2012A project team initiative.

Golf

The 2011A Golf schema messages (OTA_Golf) have been significantly enhanced (for the 2011B OpenTravel Publication) to accommodate the functionality in modern golf reservation systems. In addition, one new message pair has been added to the 1.0 XML Message Golf schema suite. Enhanced functionality includes:
• Additional golf course descriptive information, including course closures, course conditions, detailed contact information, score card information, dress policy and detailed geographical course locations (including relative and mapping coordinates)
• Enhanced tee time availability, including hourly availability, single or multiple players, restricted availability details
• Enhanced payment information, including promotions, commissions, loyalty program
• New golf service & amenities information, including equipment rentals and services available for physically challenged individuals
• Policies and fees associated with a golf booking cancellation.

The Golf Facility Information message pair allows a request for updated golf course facility information which is used to keep trading partner database(s) and cache(s) current with golf supplier facility information. Golf facility request information includes the ID and (optional) name of the golf course facility, which may be repeated to request information about multiple courses.  The Golf Facility Information response returns detailed golf facility information for the specified facility ID(s). Response information includes:
• Facility ID, name and associated facility (if the course is on a hotel property)
• Short and long descriptions (with optional club type) 
• Contact information, including phone and website
• Multimedia, including images, descriptions and movies that describe the golf facility
• Facility features, including dress policy, golf pros, on facility dining and course designer
• Available amenities, including type, description, pricing and reservation information
• Guideline tee time pricing, including minimum, maximum and average
• Location information, including physical and geo-coding
• Hours of operation
• Course conditions, including an optional source name or URL
• Policy information
• Directions
• Course closures
• Course restrictions
• Course scorecard
• Additional message functionality includes transaction processing directives that influenced search results, such as display currency.

----Other Schema Enhancements----

Enhanced Unit of Measure: To provide implementers with a more consistent and structured way to pass measurement information, the existing UnitsOfMeasureGroups (attributeGroup) was added to the OTA_HotelCommonTypes/ FeaturesType/ Feature element. Prior to this change, when information needed to be passed regarding measurements, e.g. a separate code item was used for each measurement. With the new format, implementers pass a code table item (such as “Height of light switches in guest room”) with two companion attributes: 1) the unit of measure in the @UnitOfMeasureCode, and, 2) the actual measurement in the @UnitOfMeasureQuantity.

Hotel Schema: Enhancements were made for exchanging rate plan guarantee deposit amount details in availability and booking messages; additional rate and room sorting options were added to availability messages; mandatory service indicators were added to booking messages; modification fee structures were added in addition to the existing cancellation fee structures; and user generated content rating information was added to availability and descriptive information messages.

Ground Schema: Rebate program participation information, such as “value added tax”, was added to availability, booking and notification messages.

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
If you are new to the OpenTravel specification, an Introduction to OpenTravel webinar is available at no cost. Please visit the OpenTravel website (http://opentravel.org/News/ArticleView.aspx?ArticleID=59) for a webinar schedule and instructions on how to sign up.

================
Important Notice(s)
================

==OpenTravel Schema Supporting Artifacts==

OpenTravel Code List: As part of the OpenTravel 2011 Disability Project Team work (PDF presentation included in 2011B Publication download), the following changes have been made to the OpenTravel Code List:
• Table Name Change: The existing “Physically Challenged Feature Code” list table has been renamed to “Disability Feature Code”.  To limit impact on implementers, they chose to not change the existing code list table acronym of “PHY”. All annotation references to this code list table in OpenTravel schema have been updated.
• Table Item Deprecation: Item #221 (Handicap Room) will be deprecated from the OpenTravel Room Amenity Type (RMA) code table. This deprecation will be effective with the OpenTravel 2012A Publication. Implementers are advised to use item #161 (Accessible Room) in its place.

