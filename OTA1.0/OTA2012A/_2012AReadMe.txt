=============================================
OPENTRAVEL 2012A XML MESSAGE SUITE README
=============================================

=============================
2012A Publication Contents
=============================

- The following documents are included with the OpenTravel 2012A Publication:

----------- OpenTravel_CodeTable (folder) -----------  
- OpenTravel_CodeList_2012_7_16.zip - A zip file containing the OpenTravel Code Table in Microsoft Excel format. The OpenTravel Codes List spreadsheet, included with the specification download, includes an alphabetized, point and click list of all OpenTravel Code List names (with 3 character abbreviations) and errors and warnings to help implementers quickly find code list values.

----------- OpenTravel_XML_Message_Suite_2012A (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 
- XML Instance files- Example XML instance documents in individual files that are taken directly from the use cases in the OpenTravel_MessageUserGuide_2012A.pdf.

----------- OpenTravel_2012A_Schema_Versioning.pdf ----------- 
- OpenTravel began tracking versions in the 2003B release cycle. Prior to the 2008A release, the version table contained 2001 and 2002 data for newly created messages. This document contains a table with each OpenTravel message version from 2006A through 2012A.

----------- OpenTravel_2012A_Comments_Report.pdf ----------- 
- This document contains comments that were entered against the OpenTravel 2011B specification and resulted in changes to the 2012A specification.

----------- XML_Message_Suite_Schema_Delta_2011B_TO_2012A.pdf ----------- 
- An overview of differences (delta) in schema message functionality from the 2011B publication to the 2012A publication. For each corresponding 2011B and 2012A schema XSD, there is a link in the XML Message Suite Schema Delta guide to a browser-based file that contains the results of the schema comparison in output delta format. 

----------- OpenTravel_SchemaDesignBestPracticesV3.08.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

----------- OpenTravel_2012A_XMLMessageSuite_ReleaseNotes.pdf ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2011B release and the 2012A release. 

----------- OpenTravel_2012A_Message_Users_Guide.zip ----------- 
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

================================================
2012A New Schemas and Significant Schema Updates
================================================

----New Schema----

==Air==

The OpenTravel air merchandising & operations project team created one new OpenTravel 2012A 1.0 XML Schema message pair. The focus of this project team was to provide baggage pricing, allowance and list/ catalog functionality. The new message pair, OTA_AirBaggageRQ/RS, includes the following functionality:

• Baggage Pricing
• Baggage Allowance
• Baggage List or Catalog with Pricing

Requested baggage operations may be based on a broad variety of criteria, including:

• Specific request type (Baggage Allowance, Baggage Charge, Baggage Allowance and Charge and Baggage List)
• A specified airline supplier
• A specified company (associated with the traveler)
• A specific flight
• An air reservation (PNR)
• A traveler type
• Traveler loyalty benefits
• A fare group (including private and negotiated fares)
• An origin/ destination pair
• An associated offer
• A service family (product group and subgroup)

Specific baggage information, including checked in indicator, quantity of pieces (checked bag and carry on), weight, dimensions, special item code & description, and excess baggage occurrences.

The new Air Baggage response message returns relevant offers that meet the search criteria. Returned information includes:

Allowance and Charge Information

Baggage allowance and charge by origin and destination:

• Indicator if the baggage allowance may be subject to air supplier merchandising offers
• Baggage allowance details, including weight, dimensions, special item codes & descriptions, service family and per item pricing (including currency type, amount, taxes, exchange rate details, redemption currency, pricing rules and pricing qualifiers)
• Booking and upgrade instructions
• Associated loyalty program that influenced the baggage allowance and/or pricing
• Marketing airline
• Service or bag specific fee calculation information or warnings
• Ticket box
• Airline merchandising offers that apply to baggage allowance and/or charges
• The total baggage price for the entire trip (including all passengers)

Baggage List or Priced Catalog by origin and destination:

• Marketing airline
• Baggage detail, including maximum pieces, EMD type value, allowance method, service location, and service date)
• Airline or ATPCO service family with pricing and booking instructions and booking instructions, pricing, ticket box and offers at the product subgroup level

==Golf==
The OpenTravel golf project team created one new message pair for exchanging tee time rates.

Requested rate criteria includes:

• The name of a golf course
• A date or range of dates, including days of the week, used to filter rate results
• Applied discounts that may include promotions and corporate ID's for negotiated rates
• Summary golfer type qualifying information, including quantity, age qualifier and golfer category
• Additional rate qualifiers to filter the rate results, including rate ID, rate code, rate plan type and rate category

The new Golf Rates response message returns relevant rate plan details by golf course including:

• Golf course code, ID, name, short name
• Prepaid rate indicator
• Available tee time rate indicator
• Rate details, including code, rate name, rate period, corporate discount number for special rates associated with a specific organization, promotion codes and customer loyalty program codes
• The date or range of dates, including days of the week, used to filter rate results
• Amenities included with a rate
• Constraints for the rate plan, including golfer types and facility(s) that the rate applies to
• Charge information associated with a cart rental
• Charge information associated with greens fee
• Policy(s) associated with the rate
• Rate category(s)
• Rate rules

----Significantly Enhanced Schema----

==Air==
Functionality to exchange air merchandising offers has been added to air booking path, seat management and flight details messages. 

The new AirOfferChoiceType element allows the exchange of three categories of air merchandising offers within these messages:

• Summary— Air offer information with no pricing, including offer name, short description, service family, restrictions and terms & conditions. 
• Priced (Detail)— Air offer information with no pricing, including all summary information plus pricing details—including amounts, taxes, pricing rules, pricing influencers, exchange rates and redemption amounts—seat information, booking instructions, multimedia description and commissions.
• Purchased— Information for purchased air offers, including service family and references to traveler, O&D, O&D segment and O&D flight segment that indicate the applied pricing method.

==Ground Transportation==
Additional information was added for pickup, interim stop and dropoff locations, including:
• Relative positioning (geocoding)
• An implementer-extensible list of location types, including Company, Hotel, PointOfInterest and Port
• The name of the location, which may be a hotel or airport name as an example
• Special instructions regarding the pickup, stop or drop off
• Formatted directions

Support for shuttle service was added, including:
• Multiple stop specification
• Owner & operator information
• Operation schedules, including days and hours of operation
• Ticketing & reservation information

==Hotel==
New functionality to exchange property level environmental impact and green programs & initiatives has been added to the hotel schema.

The new EnvironmentalImpactType complexType:
• Has been added as a common type in OTA_HotelCommonTypes
• Has been added as a typed element to OTA_HotelContentDescription/ HotelDescriptiveContentType named EnvironmentalImpact.
• Is available anywhere the HotelDescriptiveContentType (complexType) element is referenced, such as in HotelDescriptiveInfoRS and OTA_HotelDescriptiveContentNotifRQ.

This new type allows the exchange of the following information:
• CarbonFootprint: Carbon foot print information.
• Water: Water usage information..
• Energy: Property energy and power usage information.
• Recycling: Recycling information.
• General: Other environmental program information.

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

- OpenTravel Solution Scenarios
OpenTravel Solution Scenarios are solution scenarios designed to educate implementers on the functionality within the OpenTravel Specification by:
1. Serving as a library for code samples, best practices, and technical white papers.
2. Showcasing solution examples that are generic examples that can be re-used, repurposed or extended by developers.
3. Showcasing schema components that provide common functionality and easy integration into corporate solutions, enabling the implementer to be more efficient and consistent in building those solutions.

Visit http://wiki.opentravel.org/index.php/Public:OpenTravel_Solution_Scenarios to see a solution scenario for multimodal targeted cross-sell offers.

===================
Important Notice(s)
===================

==OpenTravel Schema==

===General Schema Maintenance===

In an effort to reduce schema binding issues, general maintenance was performed on the 2012A schema. General maintenance functionality includes:

1) Common Files Have Namespaces

     a) All common files are namespaced as xmlns:ns=http://www.opentravel.org/OTA/2003/05/common. Note that “/alpha” will be appended for draft Member Review schema and “/beta” for draft Public Review schema.
     b) All request/ response messages that include one or more common files are namespaced as xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema" xmlns="http://www.opentravel.org/OTA/2003/05/common/alpha" targetNamespace="http://www.opentravel.org/OTA/2003/05/common/alpha"

2) Nested attributeGroups have been removed
3) Enumerated types atomic base type changed from xs:NMTOKEN to xs:string
4) Additional schema extensions have been added
    a) Additional TPA_Extensions have been added throughout the specification.
     b) Open enumeration lists have been incorporated into some schema. 
          i) These contain a string list of enumerations with an "Other_" literal to support an open enumeration list. Use the "Other_" value in combination with the @extension attribute to exchange a literal that is not in the list and is known to your trading partners. 
          ii) As part of a new OpenTravel project team commencing in September, 2012, Open Lists will be created for all OpenTravel Codelists and other inline schema enumerations. 

**Note that in the 2013B OpenTravel XML Message Suite publication, the OTA_CodeType simpleType will be deprecated. All OTA_CodeType typed attributes with be replaced with elements typed as an open list, e.g. “List_NameOfList”. 

===OTA_AirAncillaryOffer.xsd vertical common file has been deprecated.===

To accommodate the new merchandising offer functionality in air booking path, seat and flight details messages and to minimize nested schema includes, the OTA_AirAncillaryOffer.xsd schema has been deprecated. The types within the OTA_AirAncillaryOffer.xsd schema have been added to the OTA_AirCommonTypes.xsd schema.

===Support for secure information exchange has been added.===

a) Support for encrypted payment and account information has been added to the specification.
b) Support for payment instrument tokenization has been added to the specification to make it easier for diverse systems to comply with PCI regulations and keep cardholder data secure. If you are not familiar with tokenization, you can find more information at http://www.shift4.com/tokenization.cfm.
c) Support for 3-D Secure protocol information has been added to the specification for online credit and debit card transactions for programs such as Verified by Visa, MasterCard SecureCode, J/Secure and SafeKey.3-D Secure.
d) Support for privacy protection via field encryption for certain combinations of elements and attributes. 

A new EncryptionTokenType element was added with the following:
Attributes

• Mask which contains a masked payment instrument element, such as xxxxxxxxxxxx9922
• Token which contains a token representing the payment instrument information, such as AEGHV234AUD54367
• EncryptionKey that contains a key required to retrieve the full payment instrument details compliant with PCI DSS standards, such as KHC32198gt4

Best Practices
OpenTravel Best Practice: Payment Instruction Tokens-Any elements containing a token value MUST NOT and WILL NOT contain unmasked card account numbers, magnetic stripe data, or card security codes (CVV2, CVC, etc.) in other attributes or elements.

Enhancement to PaymentCardType
• The @CardNumber and @SeriesCode attributes were converted to elements, with a choice of entering plain text or tokenized information (with a base type of PaymentInstrumentTokenType)
• The MagneticStripe element was converted to support plain text or payment instrument token
• The @ MaskedCardNumber attribute was deprecated.
• The @ EncryptionKey attribute was deprecated.

===Support for multimodal cross sell targeted offers===

A key emerging opportunity for travel industry suppliers is to provide targeted offers for traveler’s based on some quantity of known or derived trip and traveler characteristics. 

With the inclusion of the new MultiModalOfferType in OpenTravel schema, implementers can immediately exchange key information from a booking response in a subsequent availability request for targeted cross sell offers. 

For example, an airline supplier that has just confirmed a flight arrangement for one of their customers can send an availability request to a car supplier that contains pertinent information that allows the car supplier to return car rental offers that are complementary to the customers’ existing flight and trip information. 

OpenTravel air, cruise, golf, ground, hotel, package tour, tour & activity, rail and vehicle rental request availability messages have been enhanced with a MultimodalOffer element that contains the targeted offer influencers.
