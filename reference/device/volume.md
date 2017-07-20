# Volume

```bash
weexpack plugin add nat-device-volume
```

### get(callback)

#### Arguments
1. [`callback`] (Function)

#### Returns
1. `result` (Object)
    - `volume` (Float) (0~1)

#### Example
```js
Nat.volume.get((err, ret) => {
    console.log(ret)
})
```

### set(value, callback)

#### Arguments
1. `value` (Float) (0~1)
2. [`callback`] (Function)

#### Returns
1. `result` (Object)
    - `volume` (Float) (0~1)

#### Example
```js
Nat.volume.set(1)
```

```js
Nat.volume.set(1, (err, ret) => {
    console.log(ret)
})
```

