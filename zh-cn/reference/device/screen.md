# 屏幕 / Screen

```bash
weexpack plugin add nat-device-screen
```

### info(callback) <small class="sub">获取屏幕信息</small>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `height` (Int)
    - `width` (Int)
    - `scale` (Float)
    - `dpiX` (Int)
    - `dpiY` (Int)

#### 示例
```js
Nat.screen.info((err, ret) => {
    console.log(ret)
})
```

---

### brightness.get(callback) <small class="sub">获取屏幕亮度</small>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `brightness` (Float) (0~1)

#### 示例
```js
Nat.screen.brightness.get((err, ret) => {
    console.log(ret)
})
```

---

### brightness.set(value, callback) <small class="sub">设置屏幕亮度</small>

#### 参数
1. `value` (Float) (0~1)
2. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `brightness` (Float) (0~1)

#### 示例
```js
Nat.screen.brightness.set(1)
```

```js
Nat.screen.brightness.set(1, (err, ret) => {
    console.log(ret)
})
```

---

### orientation.status(callback) <small class="sub">获取屏幕方向状态</small>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `orientation` (String) (`portrait` | `landscape` | `landscape-left` | `landscape-right` | `portrait-down`)

#### 示例
```js
Nat.screen.orientation.status((err, ret) => {
    console.log(ret)
})
```
