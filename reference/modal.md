# Modal

### alert(params, callback)
	params: Object
		title: String
		message: String
		okButton: String (def: 'OK')
	callback: Function

### confirm(params, callback)
	params: Object
		title: String
		message: String
		okButton: String (def: 'OK')
		cancelButton: String (def: 'Cancel')
	callback: Function(ret) (Boolean)

### prompt(params, callback)
	params: Object
		title: String
		message: String
		text: String
		okButton: String (def: 'OK')
		cancelButton: String (def: 'Cancel')
	callback: Function(ret)
		retult: Boolean
		data: String

### toast(params, callback)
	params: Object
		message: String
		duration: Int (ms)
		postion: String (top | middle | bottom, def: bottom)

---

> **Error**	
> ALERT_INVALID_ARGUMENT	
> CONFIRM_INVALID_ARGUMENT	
> PROMPT_INVALID_ARGUMENT	
> TOAST_INVALID_ARGUMENT	
