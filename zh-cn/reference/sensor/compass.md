# 指南针 / Compass

```bash
weexpack plugin add nat-sensor-compass
```

### get(callback) <small class="sub">获取当前方位角</small>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `heading` (Float) (0~359.99, magnetic)

#### 示例
```js
Nat.compass.get((err, ret) => {
    console.log(ret)
})
```

---

### watch(options, callback) <small class="sub">实时监听方位角</small>
1. [`options`] (Object)
    - `interval` (Int) (ms, default: `32`)
2. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `heading` (Float) (0~359.99, magnetic)

#### 示例
```js
Nat.compass.watch((err, ret) => {
    console.log(ret)
})
```

---

### clearWatch(callback) <small class="sub">取消监听方位角</small>

#### 参数
1. [`callback`] (Function)

#### 示例
```js
Nat.compass.clearWatch(() => {
    console.log('cleared')
})
```

---

> **Error**	
> COMPASS_PERMISSION_DENIED	
> COMPASS_NOT_SUPPORTED	
> COMPASS_INTERNAL_ERROR	
> GET_COMPASS_INVALID_ARGUMENT	
> WATCH_COMPASS_INVALID_ARGUMENT	
