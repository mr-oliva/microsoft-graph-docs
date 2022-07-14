---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewDeployment()
"@odata.type" := "#microsoft.graph.windowsUpdates.deployment"
requestBody.Set"@odata.type"(&"@odata.type") 
state := graphmodels.NewDeploymentState()
requestedValue := graphmodels.PAUSED_REQUESTEDDEPLOYMENTSTATEVALUE 
state.SetRequestedValue(&requestedValue) 
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.windowsUpdates.deploymentState", 
}
state.SetAdditionalData(additionalData)
requestBody.SetState(state)

graphClient.Admin().Windows().Updates().DeploymentsById("deployment-id").Patch(requestBody)


```