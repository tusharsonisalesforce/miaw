<html>
<body>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
		embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

  window.addEventListener("onEmbeddedMessagingReady", () => {
    console.log("Received the onEmbeddedMessagingReady event…");

// Send data to Salesforce
embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({"Customer_Hash" : "11098324"});
});

embeddedservice_bootstrap.init(
	'00D0p0000008ecL',
	'MIAW_Croma_Deployment',
	'https://infinitiretaillimited--uat.sandbox.my.site.com/ESWMIAWCromaDeployment1738054455202',
	{
		scrt2URL: 'https://infinitiretaillimited--uat.sandbox.my.salesforce-scrt.com'
	}
);
} catch (err) {
console.error('Error loading Embedded Messaging: ', err);
}
	};
</script>
<script type='text/javascript' src='https://infinitiretaillimited--uat.sandbox.my.site.com/ESWMIAWCromaDeployment1738054455202/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</body>
</html>
