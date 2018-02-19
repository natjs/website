# 地理定位 / Geolocation

```bash
weexpack plugin add nat-geolocation
```

### get(callback) <small class="sub">获取当前定位</small>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
	- `latitude` (Float)
	- `longitude` (Float)
	- `speed` (Float) (m/s)
	- `accuracy` (Int) (m)

#### 示例
```js
Nat.geolocation.get((err, ret) => {
	console.log(ret)
})
```

---

### watch(options, callback) <small class="sub">实时监听定位</small>
1. [`options`] (Object)
	- `maximumAge` (Int) (ms)
	- `timeout` (Int) (ms)
	- `model` (String) (`highAccuracy` | `lowAccuracy`, default: `highAccuracy`)
2. [`callback`] (Function)

#### 返回
1. `result` (Object)
	- `latitude` (Float)
	- `longitude` (Float)
	- `speed` (Float) (m/s)
	- `accuracy` (Int) (m)

#### 示例
```js
Nat.geolocation.watch((err, ret) => {
	console.log(ret)
})
```

---

### clearWatch(callback) <small class="sub">取消监听定位</small>

#### 参数
1. [`callback`] (Function)

#### 示例
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
