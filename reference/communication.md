# Communication

### call(to, callback)
	to: String

### mail(to, params, callback)
	to: Array
	params: Object
		subject: String
		body: String
		(*) attachments: Array

### sms(to, text, callback)
	to: Array
	text: String

---

> **Error**	
> CALL_PHONE_PERMISSION_DENIED	
> SEND_SMS_PERMISSION_DENIED	
> CALL_INVALID_ARGUMENT	
> SMS_INVALID_ARGUMENT	
> MAIL_INVALID_ARGUMENT	