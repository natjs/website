# Screen

```bash
weexpack plugin add nat-device-screen
```

### info(callback)

#### Arguments
1. [`callback`] (Function)

#### Returns
1. `result` (Object)
    - `height` (Int)
    - `width` (Int)
    - `scale` (Float)
    - `dpiX` (Int)
    - `dpiY` (Int)

#### Example
```js
Nat.screen.info((err, ret) => {
    console.log(ret)
})
```

---

### brightness.get(callback)

#### Arguments
1. [`callback`] (Function)

#### Returns
1. `result` (Object)
    - `brightness` (Float) (0~1)

#### Example
```js
Nat.screen.brightness.get((err, ret) => {
    console.log(ret)
})
```

---

### brightness.set(value, callback)

#### Arguments
1. `value` (Float) (0~1)
2. [`callback`] (Function)

#### Returns
1. `result` (Object)
    - `brightness` (Float) (0~1)

#### Example
```js
Nat.screen.brightness.set(1)
```

```js
Nat.screen.brightness.set(1, (err, ret) => {
    console.log(ret)
})
```

---

### orientation.status(callback)

#### Arguments
1. [`callback`] (Function)

#### Returns
1. `result` (Object)
    - `orientation` (String) (`portrait` | `landscape` | `landscape-left` | `landscape-right` | `portrait-down`)

#### Example
```js
Nat.screen.orientation.status((err, ret) => {
    console.log(ret)
})
```

