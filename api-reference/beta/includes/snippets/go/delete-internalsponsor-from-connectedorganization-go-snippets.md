---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

connectedOrganizationId := "connectedOrganization-id"
directoryObjectId := "directoryObject-id"
graphClient.IdentityGovernance().EntitlementManagement().ConnectedOrganizationsById(&connectedOrganizationId).InternalSponsorsById(&directoryObjectId).$ref().Delete()


```