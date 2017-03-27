# Geolocation

### get(callback)
	callback: Function(err, ret)
		latitude: Float
		longitude: Float
		speed: Float (m/s)
		accuracy: Int (m)

### watch(options, callback)
	options: Object
		maximumAge: Int (ms)
		timeout: Int (ms)
		model: String (def: highAccuracy)
	callback: Function(err, ret)
		latitude: Float
		longitude: Float
		speed: Float (m/s)
		accuracy: Int (m)

### clearWatch(callback)
	callback: Function(err, ret)

---

> **Error**	
> LOCATION_INTERNAL_ERROR	
> LOCATION_NOT_SUPPORTED	
> LOCATION_PERMISSION_DENIED	
> LOCATION_SERVICE_BUSY	
> GET_LOCATION_INVALID_ARGUMENT	
> WATCH_LOCATION_INVALID_ARGUMENT	
> LOCATION_UNAVAILABLE	
> LOCATION_TIMEOUT	
