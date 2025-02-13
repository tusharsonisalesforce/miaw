<html>
<body>
 
<script type='text/javascript'>
	
	function initEmbeddedMessaging() {
		try {
		embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

  window.addEventListener("onEmbeddedMessagingReady", () => {
    console.log("Received the onEmbeddedMessagingReady event…");

// Send data to Salesforce
//embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({"Service" : "11098324"});

embeddedservice_bootstrap.userVerificationAPI.setIdentityToken({
        identityTokenType: "JWT",
        identityToken: 'eyJraWQiOiIxMjM0NSIsImFsZyI6IlJTMjU2In0.eyJpc3MiOiJ0ZXN0SXNzdWVyIiwic3ViIjoidXNlcjEiLCJleHAiOjE3MzU4MDI2MDIsImlhdCI6MTczNTc5NjYwMn0.FHc0GuF3vbvp83MfQBMf2uglmAW07Q9W0bfcz8oVaN3cco6cjUXAZzU67-n-GmY4FSjSFSB7DP5t_m8wrh18y4MgXZBtHHf0kLylG_jyXpt6ZYLhhXi9jPEk6whUGiyi1y0425QAh4KH8QyNryF1tnu7TTHS76q2hG0mEIp8h4OVivf8G43FqpWdUnV6_bHfSAJOs6ptdgoq0QQGg1KPFSOHngFtFbcwYCSkl7v9RzWoIfhIZhbzlqzJvDJo-MM8Au22RCI9Uk1KtLWUJERE8KC-bAzQoFAq89OkpLXvjiSzyoydn6CwN9ll0KlP9iH4w3sZg_hY73xJkVp4O8eNSg'
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
