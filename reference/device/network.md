# Network

```bash
weexpack plugin add nat-device-network
```

### status(callback)

#### Arguments
1. [`callback`] (Function)

#### Returns
1. `result` (Object)
    - `type` (String) (`wifi` | `3g` | `4g` | `2g` | `unkown`)

#### Example
```js
Nat.network.status((err, ret) => {
    console.log(ret)
})
```
