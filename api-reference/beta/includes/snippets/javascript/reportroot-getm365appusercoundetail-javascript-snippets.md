---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let report = await client.api('/reports/getM365AppUserDetail(period='D7')')
	.version('beta')
	.get();

```