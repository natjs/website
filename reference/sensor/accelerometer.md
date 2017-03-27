# Accelerometer

### get(callback)
	callback: Function(err, ret)
		x: Float (m/s^2)
		y: Float (m/s^2)
		z: Float (m/s^2)

### watch(options, callback)
	options: Object
		interval: Int (ms, def: 100)
	callback: Function(err, ret)
		x: Float
		y: Float
		z: Float

### clearWatch(callback)
	callback: Function(err, ret)

---

> **Error**	
> ACCELEROMETER_PERMISSION_DENIED	
> ACCELEROMETER_NOT_SUPPORTED	
> ACCELEROMETER_INTERNAL_ERROR	
> GET_ACCELERATION_INVALID_ARGUMENT	
> WATCH_ACCELERATION_INVALID_ARGUMENT	

