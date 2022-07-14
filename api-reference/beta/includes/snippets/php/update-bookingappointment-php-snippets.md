---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new BookingAppointment();
$requestBody->set@odatatype('#microsoft.graph.bookingAppointment');

$end = new DateTimeTimeZone();
$end->setDateTime('2018-05-06T12:30:00.0000000+00:00');

$end->setTimeZone('UTC');

$additionalData = [
'@odata.type' => '#microsoft.graph.dateTimeTimeZone', 
];
$end->setAdditionalData($additionalData);



$requestBody->setEnd($end);
$invoiceDate = new DateTimeTimeZone();
$invoiceDate->setDateTime('2018-05-06T12:30:00.0000000+00:00');

$invoiceDate->setTimeZone('UTC');

$additionalData = [
'@odata.type' => '#microsoft.graph.dateTimeTimeZone', 
];
$invoiceDate->setAdditionalData($additionalData);



$requestBody->setInvoiceDate($invoiceDate);
$start = new DateTimeTimeZone();
$start->setDateTime('2018-05-06T12:00:00.0000000+00:00');

$start->setTimeZone('UTC');

$additionalData = [
'@odata.type' => '#microsoft.graph.dateTimeTimeZone', 
];
$start->setAdditionalData($additionalData);



$requestBody->setStart($start);


$graphServiceClient->bookingBusinessesById('bookingBusiness-id')->appointmentsById('bookingAppointment-id')->patch($requestBody);


```