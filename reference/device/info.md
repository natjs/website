# Info

```bash
weexpack plugin add nat-device-info
```

### info(callback)

#### Arguments
1. [`callback`] (Function)

#### Returns
1. `result` (Object)
    - `model` (String)
    - `vendor` (String)
    - `uuid` (String)
    - `platform` (String) (`Android` | `iOS`)
    - `version` (String)
    - `isVirtual` (Boolean) (*iOS Only*)

#### Example
```js
Nat.device.info((err, ret) => {
    console.log(ret)
})
```
