# 加速器 / Accelerometer

```bash
weexpack plugin add nat-sensor-accelerometer
```

### get(callback) <small class="sub">获取当前加速度</small>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
	- `x` (Float) (m/s^2)
	- `y` (Float) (m/s^2)
	- `z` (Float) (m/s^2)

#### 示例
```js
Nat.accelerometer.get((err, ret) => {
	console.log(ret)
})
```

---

### watch(options, callback) <small class="sub">实时监听加速度</small>

#### 参数
1. [`options`] (Object)
	- `interval` (Int) (ms, default: `32`)
2. [`callback`] (Function)

#### 返回
1. `result` (Object)
	- `x` (Float) (m/s^2)
	- `y` (Float) (m/s^2)
	- `z` (Float) (m/s^2)

#### 示例
```js
Nat.accelerometer.watch((err, ret) => {
	console.log(ret)
})
```

---

### clearWatch(callback) <small class="sub">取消监听加速度</small>

#### 参数
1. [`callback`] (Function)

#### 示例
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

