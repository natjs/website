# Accelerometer

```bash
weexpack plugin add nat-sensor-accelerometer
```

### get(callback)

#### Arguments
1. [`callback`] (Function)

#### Returns
1. `result` (Object)
	- `x` (Float) (m/s^2)
	- `y` (Float) (m/s^2)
	- `z` (Float) (m/s^2)

#### Example
```js
Nat.accelerometer.get((err, ret) => {
	console.log(ret)
})
```

---

### watch(options, callback)
1. [`options`] (Object)
	- `interval` (Int) (ms, default: `32`)
2. [`callback`] (Function)

#### Returns
1. `result` (Object)
	- `x` (Float) (m/s^2)
	- `y` (Float) (m/s^2)
	- `z` (Float) (m/s^2)

#### Example
```js
Nat.accelerometer.watch((err, ret) => {
	console.log(ret)
})
```

---

### clearWatch(callback)

#### Arguments
1. [`callback`] (Function)

#### Example
```js
Nat.accelerometer.clearWatch(() => {
	console.log('cleared')
})
```

---

> **Error**	
> ACCELEROMETER_PERMISSION_DENIED	
> ACCELEROMETER_NOT_SUPPORTED	
> ACCELEROMETER_INTERNAL_ERROR	
> GET_ACCELERATION_INVALID_ARGUMENT	
> WATCH_ACCELERATION_INVALID_ARGUMENT	

