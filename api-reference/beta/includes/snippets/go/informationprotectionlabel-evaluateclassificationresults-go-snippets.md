---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

headers := map[string]string{
	"User-Agent": "ContosoLOBApp/1.0",
}
configuration := &graphconfig.EvaluateClassificationResultsRequestBuilderPostRequestConfiguration{
	Headers: headers,
}
requestBody := graphmodels.NewEvaluateClassificationResultsPostRequestBody()
contentInfo := graphmodels.NewContentInfo()
format := graphmodels.DEFAULT_CONTENTFORMAT 
contentInfo.SetFormat(&format) 
identifier := null
contentInfo.SetIdentifier(&identifier) 
state := graphmodels.REST_CONTENTSTATE 
contentInfo.SetState(&state) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.contentInfo", 
	"format@odata.type" : "#microsoft.graph.contentFormat", 
	"state@odata.type" : "#microsoft.graph.contentState", 
}
contentInfo.SetAdditionalData(additionalData)
requestBody.SetContentInfo(contentInfo)


classificationResult := graphmodels.NewClassificationResult()
additionalData := map[string]interface{}{
	"sensitiveTypeId" : "cb353f78-2b72-4c3c-8827-92ebe4f69fdf", 
	"count" : int32(4) , 
	"confidenceLevel" : int32(75) , 
}
classificationResult.SetAdditionalData(additionalData)

classificationResults := []graphmodels.ClassificationResultable {
	classificationResult,

}
requestBody.SetClassificationResults(classificationResults)

result, err := graphClient.InformationProtection().Policy().Labels().EvaluateClassificationResults().PostWithRequestConfigurationAndResponseHandler(requestBody, configuration, nil)


```