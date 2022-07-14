---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new EdiscoveryCaseSettings();
$requestBody->set@odatatype('#microsoft.graph.security.ediscoveryCaseSettings');

$redundancyDetection = new RedundancyDetectionSettings();
$additionalData = [
'@odata.type' => 'microsoft.graph.security.redundancyDetectionSettings', 
];
$redundancyDetection->setAdditionalData($additionalData);



$requestBody->setRedundancyDetection($redundancyDetection);
$topicModeling = new TopicModelingSettings();
$additionalData = [
'@odata.type' => 'microsoft.graph.security.topicModelingSettings', 
];
$topicModeling->setAdditionalData($additionalData);



$requestBody->setTopicModeling($topicModeling);
$ocr = new OcrSettings();
$additionalData = [
'@odata.type' => 'microsoft.graph.security.ocrSettings', 
];
$ocr->setAdditionalData($additionalData);



$requestBody->setOcr($ocr);


$graphServiceClient->security()->cases()->ediscoveryCasesById('ediscoveryCase-id')->settings()->patch($requestBody);


```