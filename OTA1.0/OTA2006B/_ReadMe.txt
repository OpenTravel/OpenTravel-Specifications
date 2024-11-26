OTA 2006B Publication Release Notes

The following documents are included with 2006B Publication:


OTA_CodeTable (folder) 
	OTA_CodeTable20061211.xls- OTA Code Tables in Microsoft Excel format. 
	OTA_CodeTable20061211.xml- OTA Code Tables in XML format. 
	OTA_CodeTable.xsd- OTA XML Schema that are used to validate the OTA Code Tables in XML format. 

OTA2006B_XML (folder) 
	OTA Schema files- OTA XML Schema messages. 
	OTA Instance files- Example XML instance documents in individual files that are taken directly from the OTA_MessageUsersGuide2006BV1.0.pdf.

OTA2006B_XMLFlattenedSchema (folder) 
	FS_<>.xsd- OTA XML Schema messages within which the reference(s) to included Schemas has been removed. These Schemas are referred to as 'flattened' since only the necessary content from included Schema files has been 'copied' into a message Schema. For instance, an OTA Schema may include several other Schema files. The 'flattened' rendition of this same Schema will contain all content from those included Schema files--but only the content that is needed (referenced) by the including Schema. OTA consumers may find that these 'flattened' Schemas provide some performance enhancements when used within an application. 

OTA_MessageUsersGuide2006BV1.0.pdf- The Message Users Guide contains a description of each OTA Message with sample use cases and XML instance documents. It provides a high-level overview of message functionality. 

OTA_SchemaDesignBestPracticesV3.04.pdf- The OTA XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OTA to ensure that the creation of XML Schemas is consistent in design across the organization and across releases. 

OTA_TransportProtocolReference_HTTPV1.0.pdf- This document contains guidance that describes how implementers should use HTTP (Hypertext Transfer Protocol) in regards to OTA message exchange.

OTA_ImplementationGuide_WSDLV1.0.pdf- This document contains best practices for building WSDL (Web Services Description Language) files for use with the OTA specification.

OTA_TransportProtocolReference_SOAPV1.0.pdf- This document contains guidance that describes how implementers should use SOAP (Simple Object Access Protocol) in regards to OTA message exchange. These guidelines include best practices for areas such as message structure, transport method (RPC vs. messaging), error handling, SOAP security and SOAP attachments. Specifications of transport protocols has not formally been a part of the OTA Specifications, and this document is intended to bridge the gap between the OTA specifications and the SOAP specification.

OTA2006BReleaseNotes.pdf- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2006A release and the 2006B release. 


** Also available via the Internet is a Reference Guide, which is an auto-generated set of web pages that allow the display of and navigation through the annotations within the XML Schemas. It provides documentation at the “field-level” detailing the use of individual elements and attributes. This is available at http://www.opentravel.org/2006B/ using the link OTA 2006B XSDdoc. 


============
Special Note
============

Excerpts from the W3C XML Schema Primer:

"In an instance document, the attribute xsi:schemaLocation provides hints from the author to a processor regarding the location of schema documents. The author warrants that these schema documents are relevant to checking the validity of the document content, on a namespace by namespace basis."

"The schemaLocation attribute contains pairs of values: The first member of each pair is the namespace for which the second member is the hint describing where to find to an appropriate schema document. The presence of these hints does not require the processor to obtain or use the cited schema documents, and the processor is free to use other schemas obtained by any suitable means, or to use no schema at all."

The intended OTA Schema is listed as the second value in each xsi:schemaLocation in each example instance. This Schema is available as part of the OTA download. Please be aware that your individual processors may treat this declaration in a variety of manners (e.g., an absolute path may be required to obtain a valid parse of the example instances).




Based on the 2006B Project Team Proposals the following Schemas have been created or updated:

OTA_AirDemandTicketRQ/RS - The Demand Ticketing Request and Response message pair provides an air travel ticketing product used for requesting ticket fulfillment.

OTA_AirCheckInRQ/RS - These messages will allow customers to check-in for eligible flights using various channels (kiosks, web and mobile) and to provide the ability to perform related functions such as checking baggage, issue bag tags, boarding passes and entering further passenger information (APIS data etc.).

OTA_AuthorizationRQ/RS - Supports the ability to verify various documents (such as credit cards, drivers licenses, addresses, checks or some combination) and requests approval to make charges.

OTA_CruiseBookingDocumentRQ/RS - The Cruise Booking Document message provides the user the ability to request a document type and its delivery method without retrieving the reservation.

OTA_ReadRQ/OTA_CruiseBookingHistoryRS - The Booking History message requests the change/service history on an existing reservation.

OTA_CruiseFastSellRQ - The Fast Sell message is a multi-purpose request to access one of the following cruise provider functions:
1. Cabin Hold (maximum of 4 cabins) when a cabin number is provided, 
2. Cabin availability when a cabin number is not provided and a category is provided,
3. Category availability when neither cabin, nor category is specified in the request.
4. Package availability when the package is specified, but not available for the sailing.
The response is conditional upon inventory availability for the requested function. If cabin is unavailable for hold, the response will be cabin availability. If category is unavailable, the response will be category availability. If the sailing or package is not available, the response will be sailing or package availability.

OTA_CruiseInfoRQ/RS – The Cruise Information message requests miscellaneous information on cruise ship statistics, embark/debark time for the cruise, cruise policy, cruise line contact, etc.

OTA_CruiseBookingPaymentRQ/RS - The Cruise Booking Payment message provides the user with the ability to submit payments for an already existing reservation without retrieving the reservation.

OTA_HotelEventRQ/RS - Serves to communicate the meeting planners event needs to a event host facility (ies).  The Hotel Event message communicates planner needs ranging from meeting room setup needs, audiovisual needs, catering needs, safety and security needs among other meeting and event requirements.

OTA_PurchaseItemRQ/RS - The purpose of this message is to electronically purchase non-inventory items ( e.g. gift certificates, drink tickets on an airline).
