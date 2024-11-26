OTA 2006A Publication Release Notes

The following documents are included with 2006A Publication:


OTA_CodeTable (folder) 
	OTA_CodeTable20060607.xls- OTA Code Tables in Microsoft Excel format. 
	OTA_CodeTable20060607.xml- OTA Code Tables in XML format. 
	OTA_CodeTable.xsd- OTA XML Schema that are used to validate the OTA Code Tables in XML format. 

OTA2006A_XML (folder) 
	OTA Schema files- OTA XML Schema messages. 
	OTA Instance files- Example XML instance documents in individual files that are taken directly from the OTA_MessageUsersGuide2006AV1.0.pdf.

OTA2006A_XMLFlattenedSchema (folder) 
	FS_<>.xsd- OTA XML Schema messages within which the reference(s) to included Schemas has been removed. These Schemas are referred to as 'flattened' since only the necessary content from included Schema files has been 'copied' into a message Schema. For instance, an OTA Schema may include several other Schema files. The 'flattened' rendition of this same Schema will contain all content from those included Schema files--but only the content that is needed (referenced) by the including Schema. OTA consumers may find that these 'flattened' Schemas provide some performance enhancements when used within an application. 

OTA_MessageUsersGuide2006AV1.0.pdf- The Message Users Guide contains a description of each OTA Message with sample use cases and XML instance documents. It provides a high-level overview of message functionality. 

OTA_SchemaDesignBestPracticesV3.04.pdf- The OTA XML Schema Best Practices document contains documentation about the standards and best practices used in creating the XML Schemas. Typically, this document is used within the OTA to ensure that the creation of XML Schemas is consistent in design across the organization and across releases. 

OTA_TransportProtocolReference_HTTPV1.0.pdf- This document contains guidance that describes how implementers should use HTTP (Hypertext Transfer Protocol) in regards to OTA message exchange.

OTA_ImplementationGuide_WSDLV1.0.pdf- This document contains best practices for building WSDL (Web Services Description Language) files for use with the OTA specification.

OTA_TransportProtocolReference_SOAPV1.0.pdf- This document contains guidance that describes how implementers should use SOAP (Simple Object Access Protocol) in regards to OTA message exchange. These guidelines include best practices for areas such as message structure, transport method (RPC vs. messaging), error handling, SOAP security and SOAP attachments. Specifications of transport protocols has not formally been a part of the OTA Specifications, and this document is intended to bridge the gap between the OTA specifications and the SOAP specification.

OTA2006AReleaseNotes.pdf- The release notes detail the latest information and changes for any given release. This file contains detailed documentation on changes made between the 2005B release and the 2006A release. 

OTA_Sponsors.pdf- This file contains special thanks to OTA sponsors.


** Also available via the Internet is a Reference Guide, which is an auto-generated set of web pages that allow the display of and navigation through the annotations within the XML Schemas. It provides documentation at the “field-level” detailing the use of individual elements and attributes. This is available at http://www.opentravel.org/2006A/ using the link OTA 2006A XSDdoc. 


============
Special Note
============

Excerpts from the W3C XML Schema Primer:

"In an instance document, the attribute xsi:schemaLocation provides hints from the author to a processor regarding the location of schema documents. The author warrants that these schema documents are relevant to checking the validity of the document content, on a namespace by namespace basis."

"The schemaLocation attribute contains pairs of values: The first member of each pair is the namespace for which the second member is the hint describing where to find to an appropriate schema document. The presence of these hints does not require the processor to obtain or use the cited schema documents, and the processor is free to use other schemas obtained by any suitable means, or to use no schema at all."

The intended OTA Schema is listed as the second value in each xsi:schemaLocation in each example instance. This Schema is available as part of the OTA download. Please be aware that your individual processors may treat this declaration in a variety of manners (e.g., an absolute path may be required to obtain a valid parse of the example instances).




Based on the 2006A Project Team Proposals the following Schemas have been created or updated:

OTA_ReadRQ and OTA_AirDisplayQueueRS - OTA_ReadRQ has been adapted to request items for a systems internal queue (e.g., all booking files, only the first item on queue). The response provides item information or the whole booking file data as requested.

OTA_CruiseCancellationPricingRQ/RS- This addresses creating the message pair which allows the travel consumer to determine the associated costs and penalties assessed by the cruise vendor, if any, should they decide to cancel an existing cruise reservation.

OTA_CruiseDiningAvailRQ/RS- This message pair allows a client the ability to request a listing of dining arrangements offered by the cruise vendor for a specific sailing.

OTA_CruisePkgAvailRQ/RS- This message pair provides the capability to request availability of Pre or Post Cruise hotel packages associated with a specified voyage.

OTA_CruisePNR_UpdateNotifRQ/RS- This is an unsolicited message sent by the cruise vendor, used to send updated reservation information to the GDS or travel partner, so they can synchronize the booking details, in the event that changes are made directly with the cruise vendor.

OTA_CruiseShorexAvailRQ/RS- This message pair provides the client with the capability of requesting shore excursion availability for a specified voyage.

OTA_CruiseSpecialServiceAvailRQ/RS- This message pair provides the ability to request the availability of Special Services offered by the cruise vendor for a specified voyage.

OTA_CruiseItineraryDescRQ/RS- This message pair allows the customer to request the detailed itinerary of a specific sailing, such as ports and arrival/departure times.

OTA_ReadRQ.xsd and OTA_ResRetrieveRS.xsd- These Schemas were updated to include Cruise functionality.

OTA_HotelBookingRuleRQ/RS- This message pair allows a user to request detailed rule information for a specific room type or booking code for a designated property.

OTA_HotelRoomListRQ/RS- This message pair contains enhancements that meet the Convention Industry Council's APEX requirements.

OTA_VehLocDetailsNotifRQ/RS- This message pair allows a car supplier to push information to a trading partner for the purpose of adding or updating location detail information in the trading partner's system.

OTA_VehRateRuleRQ/RS- This message pair allows trading partners to request more detailed information (e.g., advance booking requirement, min/max keep requirements,etc.) on one specific rate that has been returned.
