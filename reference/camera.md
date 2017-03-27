# Camera

### captureImage(params, callback)
	params: Object
		width: Int
		height: Int
	callback: Function(err, ret)
		path: String
> format: "jpeg"

### captureVideo(params, callback)
	params: Object
		width: Int
		height: Int
	callback: Function(err, ret)
		path: String

> format: "mov"

---

> **Error**	
> CAMERA_INTERNAL_ERROR	
> CAMERA_PERMISSION_DENIED	
> CAMERA_BUSY	
> CAPTURE_IMAGE_INVALID_ARGUMENT	
> CAPTURE_VIDEO_INVALID_ARGUMENT	
