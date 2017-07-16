# Audio

```bash
weexpack plugin add nat-media-audio
```

### play(url, callback)

#### Arguments
1. `url` (String)
2. [`callback`] (function)

#### Example
```js
Nat.audio.play('http://cdn.instapp.io/nat/samples/audio.mp3')
```

```js
Nat.audio.play('http://cdn.instapp.io/nat/samples/audio.mp3', () => {
    console.log('started')
})
```

---

### pause(callback)

#### Arguments
1. [`callback`] (function)

#### Example
```js
Nat.audio.pause()
```

```js
Nat.audio.pause(() => {
    console.log('paused')
})
```

---

### stop(callback)

#### Arguments
1. [`callback`] (function)

#### Example
```js
Nat.audio.stop()
```

```js
Nat.audio.stop(() => {
    console.log('stopped')
})
```

---

> **Error**	
> MEDIA_INTERNAL_ERROR	
> MEDIA_NETWORK_ERROR	
> MEDIA_DECODE_ERROR	
> MEDIA_ABORTED	
> MEDIA_PLAYER_NOT_STARTED	
> MEDIA_FILE_TYPE_NOT_SUPPORTED	
> MEDIA_SRC_NOT_SUPPORTED	
