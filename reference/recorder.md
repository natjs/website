# Recorder

### start(options, callback)
	options: Object
		channel: String (stereo, mono, def: stereo)
		quality: String (low [8000Hz, 8bit] | standard [22050Hz, 16bit] | high [44100Hz, 16bit], def: standard)
	callback: Function(err, ret)

> format: "aac" (iOS) / "wav" (Android)

### pause(callback)
	callback: Function(err, ret)

### stop(callback)
	callback: Function(err, ret)
		path: String

---

> **Error**	
> RECORDER_INTERNAL_ERROR	
> RECORD_AUDIO_PERMISSION_DENIED	
> RECORD_AUDIO_INVALID_ARGUMENT	
> RECORDER_BUSY	
> RECORDER_NOT_STARTED	
