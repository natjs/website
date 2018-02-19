# 设备信息 / Info

```bash
weexpack plugin add nat-device-info
```

### info(callback) <span class="sub">获取信息</span>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `model` (String)
    - `vendor` (String)
    - `uuid` (String)
    - `platform` (String) (`Android` | `iOS`)
    - `version` (String)
    - `language` (String)
    - `isVirtual` (Boolean) (*iOS Only*)

#### 示例
```js
Nat.device.info((err, ret) => {
    console.log(ret)
})
```
