---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewCall()
"@odata.type" := "#microsoft.graph.call"
requestBody.Set"@odata.type"(&"@odata.type") 
direction := graphmodels.OUTGOING_CALLDIRECTION 
requestBody.SetDirection(&direction) 
subject := "Create a group call with service hosted media"
requestBody.SetSubject(&subject) 
callbackUri := "https://bot.contoso.com/callback"
requestBody.SetCallbackUri(&callbackUri) 
source := graphmodels.NewParticipantInfo()
identity := graphmodels.NewIdentitySet()
"@odata.type" := "#microsoft.graph.identitySet"
identity.Set"@odata.type"(&"@odata.type") 
application := graphmodels.NewIdentity()
"@odata.type" := "#microsoft.graph.identity"
application.Set"@odata.type"(&"@odata.type") 
displayName := "TestBot"
application.SetDisplayName(&displayName) 
id := "dd3885da-f9ab-486b-bfae-85de3d445555"
application.SetId(&id) 
identity.SetApplication(application)
source.SetIdentity(identity)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.participantInfo", 
}
source.SetAdditionalData(additionalData)
requestBody.SetSource(source)


invitationParticipantInfo := graphmodels.NewInvitationParticipantInfo()
identity := graphmodels.NewIdentitySet()
"@odata.type" := "#microsoft.graph.identitySet"
identity.Set"@odata.type"(&"@odata.type") 
user := graphmodels.NewIdentity()
"@odata.type" := "#microsoft.graph.identity"
user.Set"@odata.type"(&"@odata.type") 
displayName := "user1"
user.SetDisplayName(&displayName) 
id := "98da8a1a-1b87-452c-a713-65d3f10b5555"
user.SetId(&id) 
identity.SetUser(user)
invitationParticipantInfo.SetIdentity(identity)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.invitationParticipantInfo", 
}
invitationParticipantInfo.SetAdditionalData(additionalData)
invitationParticipantInfo1 := graphmodels.NewInvitationParticipantInfo()
identity := graphmodels.NewIdentitySet()
"@odata.type" := "#microsoft.graph.identitySet"
identity.Set"@odata.type"(&"@odata.type") 
user := graphmodels.NewIdentity()
"@odata.type" := "#microsoft.graph.identity"
user.Set"@odata.type"(&"@odata.type") 
displayName := "user2"
user.SetDisplayName(&displayName) 
id := "bf5aae9a-d11d-47a8-93b1-782504c95555"
user.SetId(&id) 
identity.SetUser(user)
invitationParticipantInfo1.SetIdentity(identity)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.participantInfo", 
}
invitationParticipantInfo1.SetAdditionalData(additionalData)

targets := []graphmodels.InvitationParticipantInfoable {
	invitationParticipantInfo,
	invitationParticipantInfo1,

}
requestBody.SetTargets(targets)
requestedModalities := []graphmodels.Modalityable {
	"audio",

}
requestBody.SetRequestedModalities(requestedModalities)
mediaConfig := graphmodels.NewMediaConfig()
"@odata.type" := "#microsoft.graph.serviceHostedMediaConfig"
mediaConfig.Set"@odata.type"(&"@odata.type") 
removeFromDefaultAudioGroup := false
mediaConfig.SetRemoveFromDefaultAudioGroup(&removeFromDefaultAudioGroup) 
requestBody.SetMediaConfig(mediaConfig)
tenantId := "aa67bd4c-8475-432d-bd41-39f255720e0a"
requestBody.SetTenantId(&tenantId) 

result, err := graphClient.Communications().Calls().Post(requestBody)


```