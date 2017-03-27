# Compass

### get(callback)
	callback: Function(err, ret)
		heading: Float (0~359.99, magnetic)

### watch(options, callback)
	options: Object
		interval: Int (ms, def: 100)
	callback: Function(err, ret)
		heading: Float (0~359.99, magnetic)

### clearWatch(callback)
	callback: Function(err, ret)

---

> **Error**	
> COMPASS_PERMISSION_DENIED	
> COMPASS_NOT_SUPPORTED	
> COMPASS_INTERNAL_ERROR	
> GET_COMPASS_INVALID_ARGUMENT	
> WATCH_COMPASS_INVALID_ARGUMENT	
