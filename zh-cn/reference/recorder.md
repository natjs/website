# 录音机 / Recorder

```bash
weexpack plugin add nat-media-recorder
```

### start(options, callback) <span class="sub">开始录音</span>

#### 参数
1. `options` (Object)
    - `channel` (String) (`stereo`, `mono`, default: `stereo`)
    - `quality` (String) (`low` [8000Hz, 8bit] | `standard` [22050Hz, 16bit] | `high` [44100Hz, 16bit], default: `standard`)
2. [`callback`] (Function)

#### 示例
```js
Nat.recorder.start({
    channel: `mono`
}, () => {
    console.log('started')
})
```

---

### pause(callback) <span class="sub">暂停录音</span>

#### 参数
1. [`callback`] (Function)

#### 示例
```js
Nat.recorder.pause()
```

```js
Nat.recorder.pause(() => {
    console.log('paused')
})
```

---

### stop(callback) <span class="sub">结束录音</span>

#### 参数
1. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `path` (String)

#### 示例
```js
Nat.recorder.stop((err, ret) => {
    console.log(ret.path)
})
```

> format: "aac" (iOS) / "wav" (Android)

---

> **Error**	
> RECORDER_INTERNAL_ERROR	
> RECORD_AUDIO_PERMISSION_DENIED	
> RECORD_AUDIO_INVALID_ARGUMENT	
> RECORDER_BUSY	
> RECORDER_NOT_STARTED	
