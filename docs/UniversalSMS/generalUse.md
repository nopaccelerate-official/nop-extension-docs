# General Use

Based on the configuration set by the admin, SMS notifications will be sent to Vendors, Customers, and Admins for the events that occur. These events are configured by the admin.

**Verify OTP:**

Below is image of how customer mobile number registration screen looks like with nopCommerce default theme.

![VerifyOtp](../assets/img/SMS_VerifyOtp.png)

If you want to change the text displayed on the OTP Verification page, you can edit the following resources at **Configuration → Languages → View String Resources**:
plugins.xcellenceit.sms.fields.onetimepassword  
plugins.xcellenceit.sms.fields.onetimepassword.hint
plugins.xcellenceit.sms.fields.otpfail
plugins.xcellenceit.sms.fields.otpfheading
plugins.xcellenceit.sms.fields.otprequired
For further customization of the view page, you can edit the **RegistrationVerification.cshtml file**, which is located at:
/Plugins/XcellenceIt.Sms/Views/NopSms in your website folder.

---

## Verify OTP if Skipped During Verification:

If you skipped OTP verification earlier, you can click Verify OTP to be redirected back to the RegistrationVerification page and complete the verification process.

![CustomerEvent](../assets/img/SMS_VerifyOtpVerification.png)

[← Previous](sendTestMessageTab.md) | [Next →](developerUse.md)