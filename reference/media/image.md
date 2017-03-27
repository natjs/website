# Image

### pick(params, callback)
	params: Object
		limit: Int (def: 9)
		quality: Int (def: 100)
		width: Int
		height: Int
	callback: Function(err, ret)
		paths: Array

### preview(files, params, callback)
	files: Array
	params: Object
		current: Int (index)
		style: String (dots | label | none, def: dots)

### info(path, callback)
	path: String
	callback: Function(err, ret)
		width: Int (px)
		height: Int (px)
		type: String (png | jpeg | gif | bmp | webp | ico)

### exif(path, callback)
	path: String
	callback: Function(err, ret)
	
> See [Exif Info](http://www.cipa.jp/std/documents/e/DC-008-2012_E.pdf)

---

> **Error**	
> MEDIA_INTERNAL_ERROR	
> MEDIA_NETWORK_ERROR	
> MEDIA_DECODE_ERROR	
> MEDIA_ABORTED	
> MEDIA_PLAYER_NOT_STARTED	
> MEDIA_FILE_TYPE_NOT_SUPPORTED	
> MEDIA_SRC_NOT_SUPPORTED	
