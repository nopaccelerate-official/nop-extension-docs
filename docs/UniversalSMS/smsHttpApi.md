# SMS Http API

**SMS HTTP API:**

- You need to register with an SMS provider that provides SMS Http API.  
- Here I have registered for “smsgatewayhub” to send SMS through SMS Http API. You can register from this URL:  
  <https://www.smsgatewayhub.com/> or you can register with other SMS HTTP API providers.  
- If you have registered with 'smsgatewayhub' then go to the API document →  HTTP API tab and get API URL and if you have registered from different SMS Http API Providers then you need to get API URL from them providers.

![SmsHttpApi](../assets/img/SMS_HttpApi1.png)   

Get the API Key from SMS HTTP API providers and replace the API key in the URL and replace the country code field with the **#COUNTRYCODE#**, mobile number field with the **#MOBILENUMBER#** and message field with the **#MESSAGE#** respectively.

After replacing the fields, the URL will look like this:  
“https://www.smsgatewayhub.com/api/mt/SendSMS?APIKey=rLssEX9BxkmIHmR47t1D&senderid=WEBSMS&channel=2&DCS=0&flashsms=0&number=#MOBILENUMBER#&text=#MESSAGE#&route=clickhere”

Now go to the universal SMS plugin → configure page → interface setting tab.

![SMSHttp](../assets/img/SMS_HttpApi2.png)

- **Country:** Select the country to send SMS.  
- **Provider Interface Type:** Select SMS HTTP API.  
- **API/Gateway:** Enter your API URL with the replaced tokens and API key.
“https://www.smsgatewayhub.com/api/mt/SendSMS?APIKey=rLssEX9BxkmIHmR47t1DnQ&senderid=TESTIN&channel=2&DCS=0&flashsms=0&number=#MOBILENUMBER#&text=#MESSAGE#&route=clickhere”
- **Active:** Check if Active.


[← Previous](interfaceSettingTab.md) | [Next →](twilioSmsApi.md)