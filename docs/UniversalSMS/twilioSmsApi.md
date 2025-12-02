Twilio SMS API:

- You need to register with Twilio from this URL: https://www.twilio.com/
![Registration](../assets/img/SMS_TwilioRegistration.png)

- Select programmable SMS and click on continue.  
- Enter project name or you can skip the steps unless you reach the Dashboard.
![TwilioProject](../assets/img/SMS_TwilioProject.png)

- Go to Twilio home page and you can find your Twilio credential under Project Info.
![TwilioCreditial](../assets/img/SMS_TwilioCredintials.png)

- Go To Phone Number and and click on Active number.
- Now this way you number will active and you can use further for SMS .
![TwilioPhoneNumber](../assets/img/SMS_TwilioPhone.png)

- Now go to universal SMS plugin → configure page →  interface setting tab.
![TwilioInterFace](../assets/img/sms_configuratation.jpg)

- **Country:** Select country for sending SMS.  
- **Provider Interface Type:** Select Twilio SMS API.  
- **Twilio SID:** Enter Twilio SID that you can get from Twilio account.  
- **Twilio Auth Token:** Enter Twilio auth token that you can get from Twilio account.  
- **Twilio SMS number:** Enter Twilio phone number that you can get from Twilio account.  
  **Note:** Enter phone number without country code, space, or dash.  
  For example, if your phone number is “+1 256-645-8461”, you need to enter the number in this format: **“2566458461”**.  
- **Active:** Check Active.

Note: If you configured Twilio trial account then you need to perform below steps:
- If you are using Twilio trial account then you need to verify receivers phone number from Twilio from this url “https://www.twilio.com/console/phone-numbers/verified”
![TwilioCall](../assets/img/SMS_Verifycall1.png)

Click on ("+") button to verify the reviver's phone number.
![TwilioCallVerifiy](../assets/img/SMS_Verifycall.png)

[← Previous](smsHttpApi.md) | [Next →](customerEventSettingsTab.md)