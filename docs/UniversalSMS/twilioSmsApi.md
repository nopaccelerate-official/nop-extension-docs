Twilio SMS API:

- You need to register with Twilio from this URL: https://www.twilio.com/
![Registration](../assets/img/SMS_TwilioRegistration.png)

- Select programmable SMS and click on continue.  
- Enter project name or you can skip the steps unless you reach the Dashboard.
![TwilioProject](../assets/img/SMS_TwilioProject.png)

- Go to the Twilio home page, where you can find your Twilio credentials under Project Info.
![TwilioCreditial](../assets/img/SMS_TwilioCredintials.png)

- Go to Phone Numbers and click on the Active Number.
- This will activate your number, allowing you to use it for SMS.
![TwilioPhoneNumber](../assets/img/SMS_TwilioPhone.png)

- Now go to the Universal SMS Plugin → Configure page → Interface Settings tab.
![TwilioInterFace](../assets/img/sms_configuratation.jpg)

- **Country:** Select the country for sending SMS.  
- **Provider Interface Type:**  Select Twilio SMS API.  
- **Twilio SID:** Enter the Twilio SID obtained from your Twilio account.  
- **Twilio Auth Token:** Enter the Twilio Auth Token obtained from your Twilio account.
- **Twilio SMS number:** Enter the Twilio phone number obtained from your Twilio account.  
  **Note:** Enter the phone number without the country code, spaces, or dashes.
Example: If your phone number is +1 256-645-8461, enter it as **2566458461**.  
- **Active:** Check Active to enable the configuration.

**Note (Twilio Trial Account)**: 
- If you are using a Twilio trial account, you must verify the recipient’s phone number in the Twilio Console using the following URL: “https://www.twilio.com/console/phone-numbers/verified”
![TwilioCall](../assets/img/SMS_Verifycall1.png)

Click the ( + ) button to verify the receiver’s phone number.
![TwilioCallVerifiy](../assets/img/SMS_Verifycall.png)

[← Previous](smsHttpApi.md) | [Next →](customerEventSettingsTab.md)