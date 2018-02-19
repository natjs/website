# 音量 / Volume

```bash
weexpack plugin add nat-device-volume
```

### get(callback) <small class="sub">获取音量</small>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `volume` (Float) (0~1)

#### 示例
```js
Nat.volume.get((err, ret) => {
    console.log(ret)
})
```

### set(value, callback) <small class="sub">设置音量</small>

#### 参数
1. `value` (Float) (0~1)
2. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `volume` (Float) (0~1)

#### 示例
```js
Nat.volume.set(1)
```

```js
Nat.volume.set(1, (err, ret) => {
    console.log(ret)
})
```

