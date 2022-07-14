---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new RetentionEvent();
$requestBody->set@odatatype('#microsoft.graph.security.retentionEvent');

$requestBody->setDisplayName('String');

$requestBody->setDescription('String');

$eventQueriesEventQuery1 = new EventQuery();
$additionalData = [
'@odata.type' => 'microsoft.graph.security.eventQueries', 
];
$eventQueriesEventQuery1->setAdditionalData($additionalData);



$eventQueriesArray []= $eventQueriesEventQuery1;
$requestBody->setEventQueries($eventQueriesArray);


$requestBody->setEventTriggerDateTime(new DateTime('String (timestamp)'));

$createdBy = new IdentitySet();
$createdBy->set@odatatype('microsoft.graph.identitySet');


$requestBody->setCreatedBy($createdBy);
$eventPropagationResultsEventPropagationResult1 = new EventPropagationResult();
$additionalData = [
'@odata.type' => 'microsoft.graph.security.eventPropagationResult', 
];
$eventPropagationResultsEventPropagationResult1->setAdditionalData($additionalData);



$eventPropagationResultsArray []= $eventPropagationResultsEventPropagationResult1;
$requestBody->setEventPropagationResults($eventPropagationResultsArray);


$eventStatus = new RetentionEventStatus();
$additionalData = [
'@odata.type' => 'microsoft.graph.security.retentionEventStatus', 
];
$eventStatus->setAdditionalData($additionalData);



$requestBody->setEventStatus($eventStatus);
$requestBody->setLastStatusUpdateDateTime(new DateTime('String (timestamp)'));



$requestResult = $graphServiceClient->security()->triggers()->retentionEvents()->post($requestBody);


```