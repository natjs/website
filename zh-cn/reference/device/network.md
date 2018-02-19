# 网络 / Network

```bash
weexpack plugin add nat-device-network
```

### status(callback) <span class="sub">获取网络状态</span>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `type` (String) (`wifi` | `3g` | `4g` | `2g` | `unkown`)

#### 示例
```js
Nat.network.status((err, ret) => {
    console.log(ret)
})
```
