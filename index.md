<html>
<body>
<script type='text/javascript'>
function initEmbeddedMessaging() {
try {
embeddedservice_bootstrap.settings.language = 'en_US';

embeddedservice_bootstrap.init(
	'00D0p0000008ecL',
	'Agentforce_Messaging_Deployment',
	'https://infinitiretaillimited--uat.sandbox.my.site.com/ESWAgentforceMessagingD1737696200985',
	{
		scrt2URL: 'https://infinitiretaillimited--uat.sandbox.my.salesforce-scrt.com'
	}
);	
} catch (err) {
console.error('Error loading Embedded Messaging: ', err);
}
};
</script>
<script type='text/javascript' src='https://infinitiretaillimited--uat.sandbox.my.site.com/ESWAgentforceMessagingD1737696200985/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</body>
</html>
