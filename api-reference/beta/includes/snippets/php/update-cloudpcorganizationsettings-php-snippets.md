---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new CloudPcOrganizationSettings();
$requestBody->set@odatatype('#microsoft.graph.cloudPcOrganizationSettings');

$requestBody->setOsVersion(new CloudPcOperatingSystem('windows11'));

$requestBody->setUserAccountType(new CloudPcUserAccountType('standarduser'));

$windowsSettings = new CloudPcWindowsSettings();
$windowsSettings->setLanguage('en-US');


$requestBody->setWindowsSettings($windowsSettings);
$additionalData = [
'enableMEMAutoEnroll' => true,
];
$requestBody->setAdditionalData($additionalData);




$graphServiceClient->deviceManagement()->virtualEndpoint()->organizationSettings()->patch($requestBody);


```