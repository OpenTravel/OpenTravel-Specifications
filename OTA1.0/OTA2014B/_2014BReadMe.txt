


=============================================
OPENTRAVEL 2014B README
=============================================

=============================
2014B Publication Contents
=============================

- The following documents are included with the OpenTravel 2014B Publication:

----------- OpenTravel_CodeTable (folder) -----------  
- OpenTravel_CodeList_2014_09_22.zip - A folder containing the OpenTravel Code Table zip file in Microsoft Excel format. The OpenTravel Codes List spreadsheet, included with the specification download, includes an alphabetized, point and click list of all OpenTravel Code List names (with 3 character abbreviations) and errors and warnings to help implementers quickly find code list values.

----------- OpenTravel_2014B_XML (folder) -----------
- XML Schema files- OpenTravel XML Schema messages. 

----------- OpenTravel_2014B_Schema_Versioning.pdf ----------- 
- OpenTravel began tracking versions in the 2003B release cycle. Prior to the 2008A release, the version table contained 2001 and 2002 data for newly created messages. This document contains a table with each OpenTravel message version from 2006A through 2014B.

----------- OpenTravel_2014B_Comments_Report.pdf ----------- 
- This document contains comments that were entered against the OpenTravel 2014A specification and resulted in changes to the 2014B specification.

----------- OpenTravel_SchemaDesignBestPracticesV3.08.pdf ----------- 
- The OpenTravel XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OpenTravel Alliance to ensure that the creation of XML Schemas is consistent in design across the organization and across releases.

----------- OpenTravel_2014B_XMLMessageSuite_ReleaseNotes.pdf ----------- 
- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2014A release and the 2014B release. 

----------- OpenTravel_2014B_Message_Users_Guide.zip ----------- 
- The Message Users Guide (MUG) contains a description of each OpenTravel Message.  It provides a high-level overview of message functionality. 

----------- OpenTravel_ImplementationGuide_v1.2_ExecSum.pdf -------------
- This is an executive summary of the OpenTravel Implementation Guide. The purpose of the OpenTravel Implementation Guide is to provide invaluable information to both analysts and implementers of the OpenTravel specification on how to more easily understand and build software systems that are interoperable with other travel systems using the OpenTravel schema. The full Guide is available to members of the OpenTravel Alliance via the Wiki http://wiki.opentravel.org/index.php/Public:Resources.

----------- OpenTravel_FastRez (folder) -----------
- OpenTravel_FastRez.zip: A zipped file containing OpenTravel FastRez Schema, WSDL and User Documentation.

----------- OpenTravel_Other (folder) -----------
- OpenTravel Hotel Schema Disability Audit Results: An OpenTravel Hotel Disability Project Brief artifact has been included with the OpenTravel 2011B 1.0 XML Schema Message publication. The OpenTravel Hotel Disability project was focused on a subset of the new 2010 ADA legislation that specifically applies to electronic hotel reservations and includes identifying and describing accessible features; reserving, upon request, accessible guest rooms or specific types of guest rooms and ensuring that the guest rooms requested are blocked and removed from all reservations systems; and guaranteeing the specific accessible guest room. Per the audit results, relatively few changes were made to OpenTravel Hotel schema, with one change made to one common hotel schema (OTA_HotelCommonTypes) to provide a more consistent and structured way to pass measurement information, and annotation changes made to three hotel schema (OTA_HotelCommonTypes, OTA_RailCommonTypes and OTA_RailPreferences) to accommodate renaming the OpenTravel Code List Physically Challenged Feature code table. The slide show included with the publication includes an overview of the project.

=================================================
2014B New Messages and Significant Schema Updates
=================================================

----New Schema----

Hotel

The Product Automation Team created two new OpenTravel 2014B 1.0 XML Schema message pairs.  The focus of this project team was to create messaging to handle the creation, modification and deletion of hotel products.  Hotel products are defined as Room Types, Rate Plans, the combination of a room type and rate plan or policy information.  The OTA_HotelProductsRQ/RS message set is a pull message used to request product information for specified criteria. The OTA_HotelProductNotifRQ/RS message set is a push message used to send product information for specified criteria.  The OTA_HotelProduct.xsd houses the HotelProductType that is used in both the OTA_HotelProductNotifRQ message and the OTA_HotelProductRS message.

----Modified Schema----

Common
- Added a complex type SocialMediaType to OTA_Common types to specify social media information used to be used communicate with a guest.
- Added a required attribute Type of type StringLength1to64 to SocialMediaType to identify the social media type.
- Added a required attribute UserName of type StringLength1to64 to SocialMediaType to specify the user name for the social media type.
- Added an optional attribute PreferredContactInd of type xs:boolean to SocialMediaType to indicate the preferred method of social media for communication.
- Added an optional attribute ShareMarketInd of type xs:string with the following enumerations: Yes, No, Inhert to SocialMediaType to indicate permission for sharing data for marketing purposes.
- Added an optional attribute AuthenticationMethod of type xs:string with the following enumerations:  SecurityCode, MagneticStripe to OTA_CommonTypes/PaymentCardType/CardNumber to specifiy the method used to authenticate the card.

Hotel
- Added an optional attribute TransportationCode of type OTA_CodeType to OTA_HotelReservation/TransportationInfoType to allow for the indication of the mode of transportation.
- Added an optional attribute Description of type StringLength1to64 to OTA_HotelReservation/TransportationInfoType to allow for descriptive information regarding the mode of transportation.
- Added an optional attribute NotificationRequired of type StringLength1to64 to OTA_HotelReservation/TransportationInfoType to allow for the indication of notification being required for the mode of transportation.
- Added an optional attribute TransportationID of type StringLength1to32 to OTA_HotelReservation/TransportationInfoType to allow for the specification of a unique ID for the transporation mode.
- Typed OTA_HotelProductNotifRQ/HotelProducts/HotelProduct/ValueAddInclusions/HotelAmenity/@HotelAmenityCode of type OTA_CodeType as the attribute was not typed.
- Typed OTA_HotelProductNotifRQ/HotelProducts/HotelProduct/ValueAddInclusions/MealPlan/@MealPlanCode of type OTA_CodeType as the attribute was not typed.
- Changed the minimum number of occurrences of OTA_HotelProductNotifRQ/HotelProducts/HotelProduct/BookingRules/BookingRule to be 1.
- Add an element TPA_Extensions of type TPA_ExensionsType to OTA_HotelProductNotifRQ/HotelProducts/HotelProduct.
- Changed the minimum number of occurrences of OTA_HotelProductNotifRQ/HotelProducts/HotelProduct/HotelRefs/HotelRef to be 1.
- Changed OTA_HotelProductNotifRQ/HotelProducts/HotelProduct/ValueAddInclusions/RoomUseExtension/@CheckInTime and @CheckOutTime from type TimeOrDateTimeType to xs:time to simpley support a time rather than a date and time.
- Updated the annotation of OTA_HotelProduct/HotelProducts/HotelProduct/UniqueID to make it accurate.
- Added an optional attribute OTA_HotelProductNotifRQ/HotelProducts/HotelProduct/RatePlans/RatePlan/@PaymentCollection of type xs:string with the following enumerations:  Hotel, TravelAgency,  and HotelOrAgency.
- Created a new common file called OTA_HotelProduct with a complex type called HotelProductType and move structure from OTA_HotelProductRS to the common type. Type OTA_HotelProductsRS/HotelProducts/HotelProduct of type OTA_Hotel ProductType. OTA_HotelProductsNotifRQ/HotelProducts/HotelProduct of type OTA_Hotel ProductType and extend with the attribute ProductNotifType as already existed in the message.
- Added an optional attribute OTA_HotelProduct/HotelProducts/HotelProduct/RoomTypes/RoomType/@MaxInfantOccupancy of type xs:nonNegativeInteger.
- Changed the OTA_HotelProduct/HotelProducts/HotelProduct from 0..unbounded to 1..unbounded making the element required.
- Added an optional attribute OTA_HotelProductRQ/HotelProducts/HotelProduct/RoomTypes/@ContentLevel with the following enumerations:  FullDetails, ReferenceOnly.
- Added an optional attribute OTA_HotelProductRQ/HotelProducts/HotelProduct/RatePlans/@ContentLevel with the following enumerations:  FullDetails, ReferenceOnly.
- Deleted an optional attribute OTA_HotelProductRQ/HotelProducts/HotelProduct/PolicyInfo/@SendAllInd
- Renamed the enumerations on OTA_HotelProductRQ/HotelProducts/HotelProduct/PolicyInfo/@SendCancelPolicy to FullDetails, ReferenceOnly.
- Renamed the enumerations on OTA_HotelProductRQ/HotelProducts/HotelProduct/PolicyInfo/@SendGuaranteePayment to FullDetails, ReferenceOnly.



Rail 
- Added an optional element SeatAvailabilityDetail, 0..1 occurrences was added to OTA_RailCommonTypes/AccommodationType to provide details on the seat map.
- Added an optional element Car 0..unbounded occurrences was added to OTA_RailCommonTypes/AccommodationType/SeatAvailabilityDetail to allow for the inclusion of train car details.
- Added a required attribute Number of type AlphaNumericStringLength1to14 to OTA_RailCommonTypes/AccommodationType/SeatAvailabilityDetail/Car to specify the car number.
- Added an optional element TPA_Extensions of type TPA_ExtensionsType 0..1 occurrences to OTA_RailCommonTypes/AccommodationType/SeatAvailabilityDetail/Car to allow for additional elements and attributes to be included per Trading Partner Agreement (TPA).
- Added a required element Compartment 1..unbounded occurrences to SeatAvailabilityDetail/Car 
- Added a required attribute Number of type AlphaNumericStringLength1to14 to SeatAvailabilityDetail/Car to allow for the specification of the compartment number.
- Added an optional attribute Position of type CompartmentPositionType to allow for the specification of the position of the compartment such as close to restaurant car.
- Added a required element Seat 1..unbounded occurrences to OTA_RailCommonTypes/SeatAvailabilityDetail/Car/Compartment to allow for the identification of seats in a compartment.
- Added a required attribute Number of type AlphaNumericStringLength1to14 to OTA_RailCommonTypes/SeatAvailabilityDetail/Car/Compartment/Seat to allow for the inclusion of the seat number.
- Added an optional attribute Position of type SeatPositionType to OTA_RailCommonTypes/SeatAvailabilityDetail/Car/Compartment/Seat to allow for the seat position to be identified.
- Added an optional attribute Direction of type SeatDirectionType to OTA_RailCommonTypes/SeatAvailabilityDetail/Car/Compartment/Seat to allow for the seat direction to be identified.
- Added a required attribute AvailableInd of type xs:boolean to OTA_RailCommonTypes/SeatAvailabilityDetail/Car/Compartment/Seat to identify whether or not the seat is available.
- Added an optional element TPA_Extensions of type TPA_ExtensionsType 0..1 occurrences to OTA_RailCommonTypes/SeatAvailabilityDetail/Car/Compartment/Seat to allow for additional elements and attributes to be included per Trading Partner Agreement (TPA).
- Added an optional element TPA_Extensions of type TPA_ExtensionsType 0..1 occurrences to OTA_RailCommonTypes/SeatAvailabilityDetail/Car/Compartment to allow for additional elements and attributes to be included per Trading Partner Agreement (TPA).
- Added an optional element BerthAvailabilityDetail, 0..1 occurrences was added to OTA_RailCommonTypes/AccommodationType to allow for the inclusion of berth map details.
- Added an optional element Car 0..unbounded occurrences was added to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail to allow for the inclusion of berth details.
- Added a required attribute Number of type AlphaNumericStringLength1to14 to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car to specify the berth number.
- Added an optional element TPA_Extensions of type TPA_ExtensionsType 0..1 occurrences to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car to allow for additional elements and attributes to be included per Trading Partner Agreement (TPA).
- Added a required element Compartment 0..unbounded occurrences to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car to allow for inclusion of Compartment details.
- Added a required attribute Number of type AlphaNumericStringLength1to14 to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car/Compartment to allow for the inclusion of the compartment number.
- Added an optional attribute Position of type CompartmentPositionType to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car/Compartment to allow for the inclusion of the compartment position.
- Added a required element Berth 0..unbounded to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car/Compartment to allow for inclusion of berth information.
- Added a required attribute Number of type AlphaNumericStringLength1to14 to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car/Compartment/Berth to allow for the inclusion of the berth number.
- Added an optional attribute Position of type BerthPositionTypeto OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car/Compartment/Berth to allow for the inclusion of the berth number.
- Added a required attribute AvailableInd of type xs:boolean to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car/Compartment/Berth to identify whether or not the berth is available. 
- Added an optional element TPA_Extensions of type TPA_ExtensionsType 0..1 occurrences to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car/Compartment/Berth to allow for additional elements and attributes to be included per Trading Partner Agreement (TPA).
- Added an optional element TPA_Extensions of type TPA_ExtensionsType 0..1 occurrences to OTA_RailCommonTypes/AccommodationType/BerthAvailabilityDetail/Car/Compartment to allow for additional elements and attributes to be included per Trading Partner Agreement (TPA).

Air
- Added an optional attribute AwardsOnlyFaresInd of type xs:boolean to OTA_AirPreferences/AirSearchPrefsType/VendorPref to allow for indication that only award fares should be returned.

Cruise
- Added an optional attribute PassengerType of type OTA_CodeType to OTA_CruiseCommonTypes/SearchQualifierType to identify a category for the guest.
- Added an optional attribute CruiseTheme of type StringLength1to32 to OTA_CruiseCommonTypes/SearchQualifierType to allow for the indication of a theme type for the cruise.
- Added an optional attriubte FlightIncludedInd of type xs:boolean to OTA_CruiseCommonTypes/SearchQualifierType to indicate that only cruise options that include air fare should be returned.
- Added an optional attribute PromotionCode of type xs:StringLength1to32 to OTA_CruiseCommonTypes/SearchQualifierType to specifiy a specific promotion or advertising campaign.
- Added an optional attribute ShareCabinGender of type xs:string with the following enumerations:  Female, Male, MaleAndFemale, NoPreference to OTA_CruiseCommonTypes/SearchQualifierType to indicate gender preference for the cabin.
- Added an optional attribute ShareCabinGender of type xs:string with the following enumerations:  Female, Male, MaleAndFemale, NoPreference to OTA_CruiseCommonTypes/CabinOptionType to indicate gender preference for the cabin.
- Added an optional attribute ConfirmedOccupancy of type of type xs:NonNegativeInteger to OTA_CruiseCommonTypes/CabinOptionType to specify the number of occupants currently assigned to a cabin.


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



