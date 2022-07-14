---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewEdiscoveryNoncustodialDataSource()
dataSource := graphmodels.NewdataSource()
"@odata.type" := "microsoft.graph.security.siteSource"
dataSource.Set"@odata.type"(&"@odata.type") 
additionalData := map[string]interface{}{
site := graphmodels.New()
webUrl := "https://m365x809305.sharepoint.com/sites/Design-topsecret"
site.SetWebUrl(&webUrl) 
	dataSource.SetSite(site)
}
dataSource.SetAdditionalData(additionalData)
requestBody.SetDataSource(dataSource)

result, err := graphClient.Security().Cases().EdiscoveryCasesById("ediscoveryCase-id").NoncustodialDataSources().Post(requestBody)


```