<html>
  <script type='text/javascript'>
		function initEmbeddedMessaging() {
			try {
				embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
	
				embeddedservice_bootstrap.init(
					'00D8Z000000sp44',
					'Messaging_for_In_App_and_Web_GitHub',
					'https://infallibletechiemiaw.my.site.com/ESWMessagingforInAppa1676392506026',
					{
						scrt2URL: 'https://infallibletechiemiaw.my.salesforce-scrt.com'
					}
				);
			} catch (err) {
				console.error('Error loading Embedded Messaging: ', err);
			}
		};
  </script>
  <script type='text/javascript' src='https://infallibletechiemiaw.my.site.com/ESWMessagingforInAppa1676392506026/assets/js/bootstrap.min.js'></script>
  
  <button id="launchChatButton" onclick="launchChat()">
  	Chat with our Agents!!!
  </button>
  
  <script>
      function launchChat() {
	  initEmbeddedMessaging();
          embeddedservice_bootstrap.utilAPI.launchChat()
              .then(() => {
	      	  console.log(
		      'Inside Launch Chat'
		  );
              }).catch(() => {
	      	  console.log(
		      'Inside Launch Chat catch Block'
		  );
              }).finally(() => {
	      	  console.log(
		      'Inside Launch Chat finally Block'
		  );
              });
      }
  </script>
</html>
