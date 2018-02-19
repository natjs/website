# 摄像头 / Camera

```bash
weexpack plugin add nat-camera
```

### captureImage(options, callback) <small class="sub">拍照</small>

#### 参数
1. [`options`] (Object)
	- `width` (Int)
	- `height` (Int)
2. [`callback`] (Function)

#### 返回
1. `result` (Object)
	- `path` (String)

#### 示例
```js
Nat.camera.captureImage({}, (err, ret) => {
	console.log(ret.path)
})
```

> format: "jpeg"

---

### captureVideo(options, callback) <small class="sub">录像</small>

#### 参数
1. [`options`] (Object)
	- `width` (Int)
	- `height` (Int)
2. [`callback`] (Function)

#### 返回
1. `result` (Object)
	- `path` (String)

#### 示例
```js
Nat.camera.captureVideo({}, (err, ret) => {
	console.log(ret.path)
})
```

> format: "mov"

---

> **Error**	
> CAMERA_INTERNAL_ERROR	
> CAMERA_PERMISSION_DENIED	
> CAMERA_BUSY	
> CAPTURE_IMAGE_INVALID_ARGUMENT	
> CAPTURE_VIDEO_INVALID_ARGUMENT	
