
# Nat JavaScript Bridge

## communication

#### call(to, callback)
    to: String

#### mail(to, params, callback)
    to: Array
    params: Object
        subject: String
        body: String
        (*) attachments: Array

#### sms(to, text, callback)
    to: Array
    text: String

> **Error**
> CALL_PHONE_PERMISSION_DENIED
> SEND_SMS_PERMISSION_DENIED
> CALL_INVALID_ARGUMENT
> SMS_INVALID_ARGUMENT
> MAIL_INVALID_ARGUMENT

---

## media

### image
#### pick(params, callback)
    params: Object
        limit: Int (def: 9)
        quality: Int (def: 100)
        width: Int
        height: Int
    callback: Function(err, ret)
        paths: Array

#### preview(files, params, callback)
    files: Array
    params: Object
        current: Int (index)
        style: String (dots | label | none, def: dots)

#### info(path, callback)
    path: String
    callback: Function(err, ret)
        width: Int (px)
        height: Int (px)
        type: String (png | jpeg | gif | bmp | webp | ico)

#### exif(path, callback)
    path: String
    callback: Function(err, ret)
    
> See [Exif Info](http://www.cipa.jp/std/documents/e/DC-008-2012_E.pdf)
        

### audio
#### play(path, callback)
    path: String

#### pause(callback)
#### stop(callback)

### video
#### play(path, callback)
    path: String

#### pause(callback)
#### stop(callback)

> **Error**
> MEDIA_INTERNAL_ERROR
> MEDIA_NETWORK_ERROR
> MEDIA_DECODE_ERROR
> MEDIA_ABORTED
> MEDIA_PLAYER_NOT_STARTED
> MEDIA_FILE_TYPE_NOT_SUPPORTED
> MEDIA_SRC_NOT_SUPPORTED

---

## camera

#### captureImage(params, callback)
    params: Object
        width: Int
        height: Int
    callback: Function(err, ret)
        path: String
> format: "jpeg"

#### captureVideo(params, callback)
    params: Object
        width: Int
        height: Int
    callback: Function(err, ret)
        path: String
> format: "mov"

> **Error**
> CAMERA_INTERNAL_ERROR
> CAMERA_PERMISSION_DENIED
> CAMERA_BUSY
> CAPTURE_IMAGE_INVALID_ARGUMENT
> CAPTURE_VIDEO_INVALID_ARGUMENT


---

## recorder

#### start(options, callback)
    options: Object
        channel: String (stereo, mono, def: stereo)
        quality: String (low [8000Hz, 8bit] | standard [22050Hz, 16bit] | high [44100Hz, 16bit], def: standard)
    callback: Function(err, ret)

> format: "aac" (iOS) / "wav" (Android)

#### pause(callback)
    callback: Function(err, ret)

#### stop(callback)
    callback: Function(err, ret)
        path: String

> **Error**
> RECORDER_INTERNAL_ERROR
> RECORD_AUDIO_PERMISSION_DENIED
> RECORD_AUDIO_INVALID_ARGUMENT
> RECORDER_BUSY
> RECORDER_NOT_STARTED

---

## modal
#### alert(params, callback)
    params: Object
        title: String
        message: String
        okButton: String (def: 'OK')
    callback: Function

#### confirm(params, callback)
    params: Object
        title: String
        message: String
        okButton: String (def: 'OK')
        cancelButton: String (def: 'Cancel')
    callback: Function(ret) (Boolean)

#### prompt(params, callback)
    params: Object
        title: String
        message: String
        text: String
        okButton: String (def: 'OK')
        cancelButton: String (def: 'Cancel')
    callback: Function(ret)
        retult: Boolean
        data: String

#### toast(params, callback)
    params: Object
        message: String
        duration: Int (ms)
        postion: String (top | middle | bottom, def: bottom)

> **Error**
> ALERT_AUDIO_INVALID_ARGUMENT
> CONFIRM_AUDIO_INVALID_ARGUMENT
> PROMPT_AUDIO_INVALID_ARGUMENT
> TOAST_AUDIO_INVALID_ARGUMENT

---


## network

### stream
#### fetch(options, callback)
    options: Object
        method: String (GET | POST | PUT | PATCH | DELETE | HEAD, def: GET)
        url: String
        headers: Object
        type: String (json | jsonp | text, def: json)
        body: String
        (*) credentials: String
    callback: Function(err, ret)
        status: Int
        statusText: String
        ok: Boolean (if status is 2xx)
        data: String
        headers: String

> **Error**
> FETCH_INTERNAL_ERROR
> FETCH_INVALID_ARGUMENT
> FETCH_NETWORK_ERROR

### transfer

#### download(params, callback)
#### upload(params, callback)

> **Error**
> DOWNLOAD_INTERNAL_ERROR
> DOWNLOAD_INVALID_ARGUMENT
> DOWNLOAD_NETWORK_ERROR
> UPLOAD_INTERNAL_ERROR
> UPLOAD_INVALID_ARGUMENT
> UPLOAD_NETWORK_ERROR


### websocket

#### connect
#### send
#### close

---

## geolocation

#### get(callback)
    callback: Function(err, ret)
        latitude: Float
        longitude: Float
        speed: Float (m/s)
        accuracy: Int (m)

#### watch(options, callback)
    options: Object
        maximumAge: Int (ms)
        timeout: Int (ms)
        model: String (def: highAccuracy)
    callback: Function(err, ret)
        latitude: Float
        longitude: Float
        speed: Float (m/s)
        accuracy: Int (m)

#### clearWatch(callback)
    callback: Function(err, ret)

> **Error**
> LOCATION_INTERNAL_ERROR
> LOCATION_NOT_SUPPORTED
> LOCATION_PERMISSION_DENIED
> LOCATION_SERVICE_BUSY
> GET_LOCATION_INVALID_ARGUMENT
> WATCH_LOCATION_INVALID_ARGUMENT
> LOCATION_UNAVAILABLE
> LOCATION_TIMEOUT

---

## sensor

### accelerometer

#### get(callback)
    callback: Function(err, ret)
        x: Float (m/s^2)
        y: Float (m/s^2)
        z: Float (m/s^2)

#### watch(options, callback)
    options: Object
        interval: Int (ms, def: 100)
    callback: Function(err, ret)
        x: Float
        y: Float
        z: Float

#### clearWatch(callback)
    callback: Function(err, ret)

> **Error**
> ACCELEROMETER_PERMISSION_DENIED
> ACCELEROMETER_NOT_SUPPORTED
> ACCELEROMETER_INTERNAL_ERROR
> GET_ACCELERATION_INVALID_ARGUMENT
> WATCH_ACCELERATION_INVALID_ARGUMENT

### compass

#### get(callback)
    callback: Function(err, ret)
        heading: Float (0~359.99, magnetic)

#### watch(options, callback)
    options: Object
        interval: Int (ms, def: 100)
    callback: Function(err, ret)
        heading: Float (0~359.99, magnetic)

#### clearWatch(callback)
    callback: Function(err, ret)

> **Error**
> COMPASS_PERMISSION_DENIED
> COMPASS_NOT_SUPPORTED
> COMPASS_INTERNAL_ERROR
> GET_COMPASS_INVALID_ARGUMENT
> WATCH_COMPASS_INVALID_ARGUMENT

---

## storage

### (working in progress)


---

## contacts

### (working in progress)

---

## device

#### info(callback)
    callback: Function(err, ret)
        model: String
        vendor: String
        uuid: String
        platform: String (Android / iOS)
        version: String

### vibration

#### vibrate(time, callback)
    time: Int (ms) (def: 500)

> **Error**
> VIBRATION_PERMISSION_DENIED
> VIBRATION_NOT_SUPPORTED

### screen

#### info(callback)
    callback: Function(err, ret)
        height: Int
        width: Int
        scale: Float
        dpiX: Int
        dpiY: Int

### volume

#### set(volume, callback)
    volume: Float
    callback: Function(err, ret)

#### get(callback)
    callback: Function(err, ret)


### battery

#### status(callback)
    callback: Function(err, ret)
        level: Int (0-100)
        charging: Boolean

---

