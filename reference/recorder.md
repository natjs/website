# Recorder

```bash
weexpack plugin add nat-recorder
```

### start(options, callback)

#### Arguments
1. `options` (Object)
    - `channel` (String) (`stereo`, `mono`, default: `stereo`)
    - `quality` (String) (`low` [8000Hz, 8bit] | `standard` [22050Hz, 16bit] | `high` [44100Hz, 16bit], default: `standard`)
2. [`callback`] (Function)

#### Example
```js
Nat.recorder.start({
    channel: `mono`
}, () => {
    console.log('started')
})
```

---

### pause(callback)

#### Arguments
1. [`callback`] (Function)

#### Example
```js
Nat.recorder.pause()
```

```js
Nat.recorder.pause(() => {
    console.log('paused')
})
```

---

### stop(callback)

#### Arguments
1. [`callback`] (Function)

#### Returns
1. `result` (Object)
    - `path` (String)

#### Example
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
