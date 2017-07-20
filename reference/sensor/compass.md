# Compass

```bash
weexpack plugin add nat-sensor-compass
```

### get(callback)

#### Arguments
1. [`callback`] (Function)

#### Returns
1. `result` (Object)
    - `heading` (Float) (0~359.99, magnetic)

#### Example
```js
Nat.compass.get((err, ret) => {
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
    - `heading` (Float) (0~359.99, magnetic)

#### Example
```js
Nat.compass.watch((err, ret) => {
    console.log(ret)
})
```

---

### clearWatch(callback)

#### Arguments
1. [`callback`] (Function)

#### Example
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
