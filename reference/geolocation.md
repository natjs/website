# Geolocation

```bash
weexpack plugin add nat-geolocation
```

### get(callback)

#### Arguments
1. [`callback`] (Function)

#### Returns
1. `result` (Object)
	- `latitude` (Float)
	- `longitude` (Float)
	- `speed` (Float) (m/s)
	- `accuracy` (Int) (m)

#### Example
```js
Nat.geolocation.get((err, ret) => {
	console.log(ret)
})
```

---

### watch(options, callback)
1. [`options`] (Object)
	- `maximumAge` (Int) (ms)
	- `timeout` (Int) (ms)
	- `model` (String) (`highAccuracy` | `lowAccuracy`, default: `highAccuracy`)
2. [`callback`] (Function)

#### Returns
1. `result` (Object)
	- `latitude` (Float)
	- `longitude` (Float)
	- `speed` (Float) (m/s)
	- `accuracy` (Int) (m)

#### Example
```js
Nat.geolocation.watch((err, ret) => {
	console.log(ret)
})
```

---

### clearWatch(callback)

#### Arguments
1. [`callback`] (Function)

#### Example
```js
Nat.geolocation.clearWatch(() => {
	console.log('cleared')
})
```

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
