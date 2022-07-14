---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new EducationUser();
$requestBody->set@odatatype('#microsoft.graph.educationUser');

$requestBody->setPrimaryRole(new EducationUserRole('string'));

$requestBody->setMiddleName('String');

$requestBody->setExternalSource(new EducationExternalSource('string'));

$requestBody->setExternalSourceDetail('String');

$residenceAddress = new PhysicalAddress();
$additionalData = [
'@odata.type' => 'microsoft.graph.physicalAddress', 
];
$residenceAddress->setAdditionalData($additionalData);



$requestBody->setResidenceAddress($residenceAddress);
$mailingAddress = new PhysicalAddress();
$additionalData = [
'@odata.type' => 'microsoft.graph.physicalAddress', 
];
$mailingAddress->setAdditionalData($additionalData);



$requestBody->setMailingAddress($mailingAddress);
$student = new EducationStudent();
$additionalData = [
'@odata.type' => 'microsoft.graph.educationStudent', 
];
$student->setAdditionalData($additionalData);



$requestBody->setStudent($student);
$teacher = new EducationTeacher();
$additionalData = [
'@odata.type' => 'microsoft.graph.educationTeacher', 
];
$teacher->setAdditionalData($additionalData);



$requestBody->setTeacher($teacher);
$createdBy = new IdentitySet();
$createdBy->set@odatatype('microsoft.graph.identitySet');


$requestBody->setCreatedBy($createdBy);
$requestBody->setAccountEnabled('Boolean');

$assignedLicensesAssignedLicense1 = new AssignedLicense();
$additionalData = [
'@odata.type' => 'microsoft.graph.assignedLicense', 
];
$assignedLicensesAssignedLicense1->setAdditionalData($additionalData);



$assignedLicensesArray []= $assignedLicensesAssignedLicense1;
$requestBody->setAssignedLicenses($assignedLicensesArray);


$assignedPlansAssignedPlan1 = new AssignedPlan();
$additionalData = [
'@odata.type' => 'microsoft.graph.assignedPlan', 
];
$assignedPlansAssignedPlan1->setAdditionalData($additionalData);



$assignedPlansArray []= $assignedPlansAssignedPlan1;
$requestBody->setAssignedPlans($assignedPlansArray);


$requestBody->setBusinessPhones(['String', ]);

$requestBody->setDepartment('String');

$requestBody->setDisplayName('String');

$requestBody->setGivenName('String');

$requestBody->setMail('String');

$requestBody->setMailNickname('String');

$requestBody->setMobilePhone('String');

$requestBody->setPasswordPolicies('String');

$passwordProfile = new PasswordProfile();
$additionalData = [
'@odata.type' => 'microsoft.graph.passwordProfile', 
];
$passwordProfile->setAdditionalData($additionalData);



$requestBody->setPasswordProfile($passwordProfile);
$requestBody->setOfficeLocation('String');

$requestBody->setPreferredLanguage('String');

$provisionedPlansProvisionedPlan1 = new ProvisionedPlan();
$additionalData = [
'@odata.type' => 'microsoft.graph.provisionedPlan', 
];
$provisionedPlansProvisionedPlan1->setAdditionalData($additionalData);



$provisionedPlansArray []= $provisionedPlansProvisionedPlan1;
$requestBody->setProvisionedPlans($provisionedPlansArray);


$requestBody->setRefreshTokensValidFromDateTime(new DateTime('String (timestamp)'));

$requestBody->setShowInAddressList('Boolean');

$requestBody->setSurname('String');

$requestBody->setUsageLocation('String');

$requestBody->setUserPrincipalName('String');

$requestBody->setUserType('String');

$onPremisesInfo = new EducationOnPremisesInfo();
$additionalData = [
'@odata.type' => 'microsoft.graph.educationOnPremisesInfo', 
];
$onPremisesInfo->setAdditionalData($additionalData);



$requestBody->setOnPremisesInfo($onPremisesInfo);


$requestResult = $graphServiceClient->education()->users()->post($requestBody);


```