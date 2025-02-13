<html>
<body>

// Create a custom button or invitation to launch the web chat client.
<button id="logoutButton" onclick="onUserLogout()">Logout</button>
 
<script type='text/javascript'>

	function onUserLogout() {
		
	    console.log('inside agentforce userlogout');
        embeddedservice_bootstrap.userVerificationAPI
          .clearSession()
          .then(() => {
		  console.log('clearSession Success');
		  //location.reload();
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
//embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({"Service" : "11098324"});

embeddedservice_bootstrap.userVerificationAPI.setIdentityToken({
        identityTokenType: "JWT",
        identityToken: 'eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6IjEyMzQ1In0.eyJzdWIiOiJ1c2VyMSIsImlzcyI6InRlc3RJc3N1ZXIiLCJleHAiOiI2MDAwIn0.Wag70vnLt_ZrxxS2Bd6I-0eyJPAsG-tSAUUuj4FF2mzGHf4PZ4kNx38FX2M7-DRMd72LMxDzw8kRUcFp7B8Df4_9ahWKKudouy4fONt_XX32bBR5sl7L8frZ6S2BHuI8melR_2Pa6rgeoH3nwz1eLv4f0JYLDtks7vc33lV_c-C_tCpXStmhT4v94hDi-xZUS-PKMEycfViUl5ZAXiSERHrEpPAFDHm23h3jrg_9sboEH7OU5HxOaK39nxA_swB1BCgq9Qb45XybSsLdKvP9k_RPzUckW_Gct41-abO9RSHqf4RsUZabO2mszAB8EsAR3a-T-GPrJjsHgBuJfwAg6A'
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
