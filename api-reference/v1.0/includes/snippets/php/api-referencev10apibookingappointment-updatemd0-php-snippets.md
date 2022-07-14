---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new BookingAppointment();
$requestBody->set@odatatype('#microsoft.graph.bookingAppointment');

$endDateTime = new DateTimeTimeZone();
$endDateTime->setDateTime('2018-05-06T12:30:00.0000000+00:00');

$endDateTime->setTimeZone('UTC');

$additionalData = [
'@odata.type' => '#microsoft.graph.dateTimeTimeZone', 
];
$endDateTime->setAdditionalData($additionalData);



$requestBody->setEndDateTime($endDateTime);
$startDateTime = new DateTimeTimeZone();
$startDateTime->setDateTime('2018-05-06T12:00:00.0000000+00:00');

$startDateTime->setTimeZone('UTC');

$additionalData = [
'@odata.type' => '#microsoft.graph.dateTimeTimeZone', 
];
$startDateTime->setAdditionalData($additionalData);



$requestBody->setStartDateTime($startDateTime);


$graphServiceClient->solutions()->bookingBusinessesById('bookingBusiness-id')->appointmentsById('bookingAppointment-id')->patch($requestBody);


```