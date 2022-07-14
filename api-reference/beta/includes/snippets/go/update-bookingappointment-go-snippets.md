---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewBookingAppointment()
"@odata.type" := "#microsoft.graph.bookingAppointment"
requestBody.Set"@odata.type"(&"@odata.type") 
end := graphmodels.NewDateTimeTimeZone()
dateTime := "2018-05-06T12:30:00.0000000+00:00"
end.SetDateTime(&dateTime) 
timeZone := "UTC"
end.SetTimeZone(&timeZone) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.dateTimeTimeZone", 
}
end.SetAdditionalData(additionalData)
requestBody.SetEnd(end)
invoiceDate := graphmodels.NewDateTimeTimeZone()
dateTime := "2018-05-06T12:30:00.0000000+00:00"
invoiceDate.SetDateTime(&dateTime) 
timeZone := "UTC"
invoiceDate.SetTimeZone(&timeZone) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.dateTimeTimeZone", 
}
invoiceDate.SetAdditionalData(additionalData)
requestBody.SetInvoiceDate(invoiceDate)
start := graphmodels.NewDateTimeTimeZone()
dateTime := "2018-05-06T12:00:00.0000000+00:00"
start.SetDateTime(&dateTime) 
timeZone := "UTC"
start.SetTimeZone(&timeZone) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.dateTimeTimeZone", 
}
start.SetAdditionalData(additionalData)
requestBody.SetStart(start)

graphClient.BookingBusinessesById("bookingBusiness-id").AppointmentsById("bookingAppointment-id").Patch(requestBody)


```