# Vibration

```bash
weexpack plugin add nat-device-vibration
```

### vibrate(time, callback)

#### Arguments
1. [`time`] (Int) (ms, default: `500`) (*Android Only*)
2. [`callback`] (Function)

#### Example
```js
Nat.vibrate()
```

```js
Nat.vibrate(2000)
```
---

> **Error**	
> VIBRATION_PERMISSION_DENIED	
> VIBRATION_NOT_SUPPORTED	

