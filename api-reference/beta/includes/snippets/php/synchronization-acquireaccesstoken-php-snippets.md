---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new AcquireAccessTokenPostRequestBody();
$credentialsSynchronizationSecretKeyStringValuePair1 = new SynchronizationSecretKeyStringValuePair();
$additionalData = [
'@odata.type' => 'microsoft.graph.synchronizationSecretKeyStringValuePair', 
];
$credentialsSynchronizationSecretKeyStringValuePair1->setAdditionalData($additionalData);



$credentialsArray []= $credentialsSynchronizationSecretKeyStringValuePair1;
$requestBody->setCredentials($credentialsArray);




$graphServiceClient->applicationsById('application-id')->synchronization()->acquireAccessToken()->post($requestBody);


```