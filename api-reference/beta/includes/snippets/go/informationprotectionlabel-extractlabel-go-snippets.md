---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

headers := map[string]string{
	"User-Agent": "ContosoLOBApp/1.0",
}
configuration := &graphconfig.ExtractLabelRequestBuilderPostRequestConfiguration{
	Headers: headers,
}
requestBody := graphmodels.NewExtractLabelPostRequestBody()
contentInfo := graphmodels.NewContentInfo()
format := graphmodels.DEFAULT_CONTENTFORMAT 
contentInfo.SetFormat(&format) 
identifier := null
contentInfo.SetIdentifier(&identifier) 
state := graphmodels.REST_CONTENTSTATE 
contentInfo.SetState(&state) 


keyValuePair := graphmodels.NewKeyValuePair()
name := "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Enabled"
keyValuePair.SetName(&name) 
value := "True"
keyValuePair.SetValue(&value) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.keyValuePair", 
}
keyValuePair.SetAdditionalData(additionalData)
keyValuePair1 := graphmodels.NewKeyValuePair()
name := "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Method"
keyValuePair1.SetName(&name) 
value := "Standard"
keyValuePair1.SetValue(&value) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.keyValuePair", 
}
keyValuePair1.SetAdditionalData(additionalData)
keyValuePair2 := graphmodels.NewKeyValuePair()
name := "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SetDate"
keyValuePair2.SetName(&name) 
value := "1/1/0001 12:00:00 AM"
keyValuePair2.SetValue(&value) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.keyValuePair", 
}
keyValuePair2.SetAdditionalData(additionalData)
keyValuePair3 := graphmodels.NewKeyValuePair()
name := "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_SiteId"
keyValuePair3.SetName(&name) 
value := "cfa4cf1d-a337-4481-aa99-19d8f3d63f7c"
keyValuePair3.SetValue(&value) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.keyValuePair", 
}
keyValuePair3.SetAdditionalData(additionalData)
keyValuePair4 := graphmodels.NewKeyValuePair()
name := "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_Name"
keyValuePair4.SetName(&name) 
value := "Top Secret"
keyValuePair4.SetValue(&value) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.keyValuePair", 
}
keyValuePair4.SetAdditionalData(additionalData)
keyValuePair5 := graphmodels.NewKeyValuePair()
name := "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ContentBits"
keyValuePair5.SetName(&name) 
value := "0"
keyValuePair5.SetValue(&value) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.keyValuePair", 
}
keyValuePair5.SetAdditionalData(additionalData)
keyValuePair6 := graphmodels.NewKeyValuePair()
name := "MSIP_Label_722a5300-ac39-4c9a-88e3-f54c46676417_ActionId"
keyValuePair6.SetName(&name) 
value := "00000000-0000-0000-0000-000000000000"
keyValuePair6.SetValue(&value) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.keyValuePair", 
}
keyValuePair6.SetAdditionalData(additionalData)

metadata := []graphmodels.KeyValuePairable {
	keyValuePair,
	keyValuePair1,
	keyValuePair2,
	keyValuePair3,
	keyValuePair4,
	keyValuePair5,
	keyValuePair6,

}
contentInfo.SetMetadata(metadata)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.contentInfo", 
	"format@odata.type" : "#microsoft.graph.contentFormat", 
	"state@odata.type" : "#microsoft.graph.contentState", 
	"metadata@odata.type" : "#Collection(microsoft.graph.keyValuePair)", 
}
contentInfo.SetAdditionalData(additionalData)
requestBody.SetContentInfo(contentInfo)

result, err := graphClient.InformationProtection().Policy().Labels().ExtractLabel().PostWithRequestConfigurationAndResponseHandler(requestBody, configuration, nil)


```