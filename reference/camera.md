# Camera

```bash
weexpack plugin add nat-camera
```

### captureImage(options, callback)

#### Arguments
1. [`options`] (Object)
	- `width` (Int)
	- `height` (Int)
2. [`callback`] (function)

#### Returns
1. `result` (Object)
	- `path` (String)

#### Example
```js
Nat.camera.captureImage({}, (err, ret) => {
	console.log(ret.path)
})
```

> format: "jpeg"

---

### captureVideo(options, callback)

#### Arguments
1. [`options`] (Object)
	- `width` (Int)
	- `height` (Int)
2. [`callback`] (function)

#### Returns
1. `result` (Object)
	- `path` (String)

#### Example
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
