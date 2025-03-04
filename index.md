<html>
<body>

<button id="logoutButton" onclick="onUserLogout()">Logout</button>
 
<script type='text/javascript'>

	function onUserLogout() {
		
	    console.log('inside agentforce userlogout');
	embeddedservice_bootstrap.userVerificationAPI
          .clearSession()
          .then(() => {
            console.log('clearSession Success');
            // Add actions to run after the session is cleared successfully.
          })
          .catch((error) => {
            console.log('clearSession Error');
            // Add actions to run after clearing the session fails.
          })
          .finally(() => {
            // Add actions to run whether the chat client launches
            // successfully or not.
          });
      
        // Add code to perform any other logout actions.
    }
	
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
	'Agentforce_GitHub',
	'https://infinitiretaillimited--uat.sandbox.my.site.com/ESWAgentforceGitHub1738318256114',
	{
		scrt2URL: 'https://infinitiretaillimited--uat.sandbox.my.salesforce-scrt.com'
	}
);
} catch (err) {
console.error('Error loading Embedded Messaging: ', err);
}
	};
</script>
<script type='text/javascript' src='https://infinitiretaillimited--uat.sandbox.my.site.com/ESWMIAWCromaDeployment1738054455202/assets/js/bootstrap.min.js'></script>
</body>
</html>
