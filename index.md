<html>
<body>
	<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

window.addEventListener("onEmbeddedMessagingReady", () => {
	console.log("Received the onEmbeddedMessagingReady event.");
	embeddedservice_bootstrap.userVerificationAPI.setIdentityToken({
		identityTokenType: "JWT",
		identityToken: "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6IjEyMzQ1In0.eyJzdWIiOiJ1c2VyMTAiLCJpc3MiOiJ0ZXN0SXNzdWVyIiwiZXhwIjoiNjAwMCJ9.HDC9A7fbv4BLoNqRV9rITUACuXOjFq5HpD33CawhnnGMWOtcR_i5zIqnno72i4-q3FBeSPm75gasTcdJ4shARCL_i5dCyjl0SQ91Ibj9OmWYUyZ4Y94nMYD_Bd4q-vAeX-btg-Alb7MbBF-OvkyuXM39YZVvTPW7jXoDChAhzCzoLAYSR5cqw0Py4dd4s7hAWCJDQkhZ0Yfrzx6x3ZVMljIu2XXwBvLC6UQqWYfM1TBKG7eEcG12PCbrTsMcOFYJWhLrMryYDhUV6XdNc_E_38Au7w3zYCL4DGbQXkCMFTOQXHuWEoJ2SZDZae3dQa-ZDkACXMhkNfAmdnrssQfFOQ"
	});
});

embeddedservice_bootstrap.init(
	'00DWs000007IsfR',
	'MIAW',
	'https://storm-403667cf952fd5.my.site.com/ESWMIAW1735553027652',
	{
		scrt2URL: 'https://storm-403667cf952fd5.my.salesforce-scrt.com'
	}
);
} catch (err) {
console.error('Error loading Embedded Messaging: ', err);
}
};
</script>
<script type='text/javascript' src='https://storm-403667cf952fd5.my.site.com/ESWMIAW1735553027652/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</body>
</html>
