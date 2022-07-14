---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new EvaluateRemovalPostRequestBody();
$contentInfo = new ContentInfo();
$contentInfo->setFormat(new ContentFormat('default'));

$ContentInfo->setIdentifier(null);

$contentInfo->setState(new ContentState('rest'));

$metadataKeyValuePair1 = new KeyValuePair();
$metadataKeyValuePair1->setName('MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Enabled');

$metadataKeyValuePair1->setValue('True');

$additionalData = [
'@odata.type' => '#microsoft.graph.keyValuePair', 
];
$metadataKeyValuePair1->setAdditionalData($additionalData);



$metadataArray []= $metadataKeyValuePair1;
$metadataKeyValuePair2 = new KeyValuePair();
$metadataKeyValuePair2->setName('MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Method');

$metadataKeyValuePair2->setValue('Standard');

$additionalData = [
'@odata.type' => '#microsoft.graph.keyValuePair', 
];
$metadataKeyValuePair2->setAdditionalData($additionalData);



$metadataArray []= $metadataKeyValuePair2;
$metadataKeyValuePair3 = new KeyValuePair();
$metadataKeyValuePair3->setName('MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SetDate');

$metadataKeyValuePair3->setValue('1/1/0001 12:00:00 AM');

$additionalData = [
'@odata.type' => '#microsoft.graph.keyValuePair', 
];
$metadataKeyValuePair3->setAdditionalData($additionalData);



$metadataArray []= $metadataKeyValuePair3;
$metadataKeyValuePair4 = new KeyValuePair();
$metadataKeyValuePair4->setName('MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SiteId');

$metadataKeyValuePair4->setValue('cfa4cf1d-a337-4481-aa99-19d8f3d63f7c');

$additionalData = [
'@odata.type' => '#microsoft.graph.keyValuePair', 
];
$metadataKeyValuePair4->setAdditionalData($additionalData);



$metadataArray []= $metadataKeyValuePair4;
$metadataKeyValuePair5 = new KeyValuePair();
$metadataKeyValuePair5->setName('MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Name');

$metadataKeyValuePair5->setValue('General');

$additionalData = [
'@odata.type' => '#microsoft.graph.keyValuePair', 
];
$metadataKeyValuePair5->setAdditionalData($additionalData);



$metadataArray []= $metadataKeyValuePair5;
$metadataKeyValuePair6 = new KeyValuePair();
$metadataKeyValuePair6->setName('MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ContentBits');

$metadataKeyValuePair6->setValue('0');

$additionalData = [
'@odata.type' => '#microsoft.graph.keyValuePair', 
];
$metadataKeyValuePair6->setAdditionalData($additionalData);



$metadataArray []= $metadataKeyValuePair6;
$metadataKeyValuePair7 = new KeyValuePair();
$metadataKeyValuePair7->setName('MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ActionId');

$metadataKeyValuePair7->setValue('00000000-0000-0000-0000-000000000000');

$additionalData = [
'@odata.type' => '#microsoft.graph.keyValuePair', 
];
$metadataKeyValuePair7->setAdditionalData($additionalData);



$metadataArray []= $metadataKeyValuePair7;
$contentInfo->setMetadata($metadataArray);


$additionalData = [
'@odata.type' => '#microsoft.graph.contentInfo', 
'format@odata.type' => '#microsoft.graph.contentFormat', 
'state@odata.type' => '#microsoft.graph.contentState', 
'metadata@odata.type' => '#Collection(microsoft.graph.keyValuePair)', 
];
$contentInfo->setAdditionalData($additionalData);



$requestBody->setContentInfo($contentInfo);
$downgradeJustification = new DowngradeJustification();
$downgradeJustification->setJustificationMessage('The information has been declassified.');

$downgradeJustification->setIsDowngradeJustified(true);


$requestBody->setDowngradeJustification($downgradeJustification);

$requestConfiguration = new EvaluateRemovalRequestBuilderPostRequestConfiguration();

$headers = [
'User-Agent' => 'ContosoLOBApp/1.0',
];

$requestConfiguration->headers = $headers;


$requestResult = $graphServiceClient->informationProtection()->policy()->labels()->evaluateRemoval()->post($requestBody, $requestConfiguration);


```