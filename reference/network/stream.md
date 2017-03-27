# Stream

### fetch(options, callback)
	options: Object
		method: String (GET | POST | PUT | PATCH | DELETE | HEAD, def: GET)
		url: String
		headers: Object
		type: String (json | jsonp | text, def: json)
		body: String
		(*) credentials: String
	callback: Function(err, ret)
		status: Int
		statusText: String
		ok: Boolean (if status is 2xx)
		data: String
		headers: String

---

> **Error**	
> FETCH_INTERNAL_ERROR	
> FETCH_INVALID_ARGUMENT	
> FETCH_NETWORK_ERROR	

