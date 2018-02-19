# 视频 / Video

```bash
weexpack plugin add nat-media-video
```

### play(url, callback) <span class="sub">播放视频</span>

#### 参数
1. `url` (String)
2. [`callback`] (Function)

#### 示例
```js
Nat.video.play('http://cdn.instapp.io/nat/samples/video.mp4')
```

```js
Nat.video.play('http://cdn.instapp.io/nat/samples/video.mp4', () => {
    console.log('started')
})
```

---

### pause(callback) <span class="sub">暂停视频</span>

#### 参数
1. [`callback`] (Function)

#### 示例
```js
Nat.video.pause()
```

```js
Nat.video.pause(() => {
    console.log('paused')
})
```

---

### stop(callback) <span class="sub">停止视频</span>

#### 参数
1. [`callback`] (Function)

#### 示例
```js
Nat.video.stop()
```

```js
Nat.video.stop(() => {
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
