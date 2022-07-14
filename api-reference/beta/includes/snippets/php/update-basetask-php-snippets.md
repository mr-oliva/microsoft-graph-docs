---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new BaseTask();
$requestBody->set@odatatype('#microsoft.graph.task');

$requestBody->setTextBody('String');

$requestBody->setBodyLastModifiedDateTime(new DateTime('String (timestamp)'));

$requestBody->setCompletedDateTime(new DateTime('String (timestamp)'));

$dueDateTime = new DateTimeTimeZone();
$additionalData = [
'@odata.type' => 'microsoft.graph.dateTimeTimeZone', 
];
$dueDateTime->setAdditionalData($additionalData);



$requestBody->setDueDateTime($dueDateTime);
$startDateTime = new DateTimeTimeZone();
$additionalData = [
'@odata.type' => 'microsoft.graph.dateTimeTimeZone', 
];
$startDateTime->setAdditionalData($additionalData);



$requestBody->setStartDateTime($startDateTime);
$requestBody->setImportance(new Importance('string'));

$recurrence = new PatternedRecurrence();
$additionalData = [
'@odata.type' => 'microsoft.graph.patternedRecurrence', 
];
$recurrence->setAdditionalData($additionalData);



$requestBody->setRecurrence($recurrence);
$requestBody->setDisplayName('String');

$requestBody->setStatus(new TaskStatus_v2('string'));

$viewpoint = new TaskViewpoint();
$additionalData = [
'@odata.type' => 'microsoft.graph.taskViewpoint', 
];
$viewpoint->setAdditionalData($additionalData);



$requestBody->setViewpoint($viewpoint);


$graphServiceClient->me()->tasks()->listsById('baseTaskList-id')->tasksById('baseTask-id')->patch($requestBody);


```