---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewEdiscoveryCaseSettings()
"@odata.type" := "#microsoft.graph.security.ediscoveryCaseSettings"
requestBody.Set"@odata.type"(&"@odata.type") 
redundancyDetection := graphmodels.NewRedundancyDetectionSettings()
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.security.redundancyDetectionSettings", 
}
redundancyDetection.SetAdditionalData(additionalData)
requestBody.SetRedundancyDetection(redundancyDetection)
topicModeling := graphmodels.NewTopicModelingSettings()
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.security.topicModelingSettings", 
}
topicModeling.SetAdditionalData(additionalData)
requestBody.SetTopicModeling(topicModeling)
ocr := graphmodels.NewOcrSettings()
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.security.ocrSettings", 
}
ocr.SetAdditionalData(additionalData)
requestBody.SetOcr(ocr)

graphClient.Security().Cases().EdiscoveryCasesById("ediscoveryCase-id").Settings().Patch(requestBody)


```