---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAcquireAccessTokenPostRequestBody()


synchronizationSecretKeyStringValuePair := graphmodels.NewSynchronizationSecretKeyStringValuePair()
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.synchronizationSecretKeyStringValuePair", 
}
synchronizationSecretKeyStringValuePair.SetAdditionalData(additionalData)

credentials := []graphmodels.SynchronizationSecretKeyStringValuePairable {
	synchronizationSecretKeyStringValuePair,

}
requestBody.SetCredentials(credentials)

graphClient.ApplicationsById("application-id").Synchronization().AcquireAccessToken(application-id).Post(requestBody)


```