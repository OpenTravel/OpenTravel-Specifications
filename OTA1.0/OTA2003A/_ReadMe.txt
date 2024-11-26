OTA 2003A Publication
Release Notes
May 28, 2003

Parsed against
XML Spy 5.2 and 5.4
Turbo XML 2.2
XSV (W3C)
SQC (IBM)
MSV (Sun)

New 2003A Messages
OTA_HotelResModifyRQ
OTA_HotelResModifyRS
OTA_HotelRFP_RQ
OTA_HotelRFP_RS
OTA_InsurancePlanSearchRQ
OTA_InsurancePlanSearchRS

The 2003A Files were initially released on May 21. Since that point, some updates have been made to the files that were part of the
2003A Comment review period. These updates are:

1) HotelCommonTypes.xsd
   ComplexType HotelRoomListType element AdditionalDetails made optional
   Extended HotelSearchCriterion by adding an element Award (0-5) with attributes of provider and rating
   Added CodeInfoGroup to FeaturesType/Feature and made Description optional

2) HotelContentDescription.xsd
   ComplexType PoliciesType element TaxPolicies made optional and element TaxPolicy made unbounded
   ComplexType FacilityInfoType element Codes under element MeetingRooms made optional
   ComplexType RestaurantsType element ContactInfos under element Restaurant made optional
   ComplexType PoliciesType element PolicyInfo attributes CheckInTime and CheckOutTime made to be TimeOrDateTime
   Added CodeInfoGroup to AreaInfoType/Recreations/Recreation and ContactsType/Name

3) OTA_PkgCommonTypes
   Changed occurrence in RoomPriceType/ ItemPrice (0,5) and ProfilePrice (0,1) and removed the reference to currency in the
annotation
