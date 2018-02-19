# 电池 / Battery

```bash
weexpack plugin add nat-device-battery
```

### status(callback) <span class="sub">获取电池状态</span>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `level` (Int) (0~100)
    - `isPlugged` (Boolean)

#### 示例
```js
Nat.battery.status((err, ret) => {
    console.log(ret)
})
```
