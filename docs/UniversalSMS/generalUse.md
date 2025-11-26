# General Use

As per the configuration set by admin, SMS will be sent to Vendor, Customer and Admin regarding the event that took place. The event is configured by the admin.

**Verify OTP:**

Below is image of how customer mobile number registration screen looks like with nopCommerce default theme.



If you want to change text displayed on OTP Verification page, you can find and edit following at **Configuration → Languages → View string resources.**

plugins.xcellenceit.sms.fields.onetimepassword  
plugins.xcellenceit.sms.fields.onetimepassword.hint  
plugins.xcellenceit.sms.fields.otpfail  
plugins.xcellenceit.sms.fields.otpfheading  
plugins.xcellenceit.sms.fields.otprequired  

For further customization in view page, you can find **"RegistrationVerification.cshtml"** placed at  
“/Plugins/XcellenceIt.Sms/Views/NopSms” directory in your website folder.

---

## Verify OTP if Skip while verification:

If you want to verify OTP then you can click on verify OTP it will again redirect to RegistrationVerification page.
