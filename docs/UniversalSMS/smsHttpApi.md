# SMS Http API

**SMS Http API:**

- You need to register with any SMS provider that provides SMS Http API.  
- Here I have registered for “smsgatewayhub” for send SMS through SMS Http API. You can register from this URL:  
  <https://www.smsgatewayhub.com/> or you can register from different SMS Http API Providers.  
- If you have registered in “smsgatewayhub” then Go to API Document → Http API Tab and get API URL and if you have registered from different SMS Http API Providers then you need to get API URL from that providers.

![SmsHttpApi](../assets/img/SMS_HttpApi1.png)   

Get API Key from SMS Http API Providers and replace API key in URL and replace country code field with **#COUNTRYCODE#**, mobile number field with **#MOBILENUMBER#** and message field with **#MESSAGE#** respectively.

After replacing fields URL will look like this:  
“https://www.smsgatewayhub.com/api/mt/SendSMS?APIKey=rLssEX9BxkmIHmR47t1D&senderid=WEBSMS&channel=2&DCS=0&flashsms=0&number=#MOBILENUMBER#&text=#MESSAGE#&route=clickhere”

Now go to universal SMS plugin → configure page → interface setting tab.

![SMSHttp](../assets/img/SMS_HttpApi2.png)

- **Country:** Select country for send SMS.  
- **Provider Interface Type:** Select SMS Http Api.  
- **API/Gateway:** Enter your API URL with replaced tokens and API key.
“https://www.smsgatewayhub.com/api/mt/SendSMS?APIKey=rLssEX9BxkmIHmR47t1DnQ&senderid=TESTIN&channel=2&DCS=0&flashsms=0&number=#MOBILENUMBER#&text=#MESSAGE#&route=clickhere”
- **Active:** Check Active.


[← Previous](interfaceSettingTab.md) | [Next →](twilioSmsApi.md)