# 文件传输 / Transfer

```bash
weexpack plugin add nat-transfer
```

### download(url, options, hooks, callback) <span class="sub">下载</span>

#### 参数
1. `url` (String)
2. [`options`] (Object)
    - `headers` (Object)
    - `target` (String)
3. [`hooks`] (Object)
    - `onProgress` (Function)
4. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `status` (Int)
    - `statusText` (String)
    - `ok` (Boolean) (status `2xx`)
    - `headers` (String)
    - `data` (String)

#### 示例
```js
Nat.download('http://cdn.instapp.io/nat/samples/audio.mp3', (err, ret) => {
    console.log(ret)
})
```

```js
Nat.download('http://cdn.instapp.io/nat/samples/audio.mp3', {
    headers: {
        'x-app': 'nat/0.0.8',
        'x-sign': 'bfbbf4c1f087d972'
    },
    target: '/instapp/nat/download'
}, {
    onProgress: (p) => {
        console.log('Progressing: ' + p)
    }
}, (err, ret) => {
    console.log(ret)
})
```

---

### upload(url, options, hooks, callback) <span class="sub">上传</span>

#### 参数
1. `url` (String)
2. `options` (Object)
    - `path` (String)
    - [`method`] (String) (`POST` | `PUT` | `PATCH`, default: `POST`)
    - [`headers`] (Object)
    - [`name`] (String)
    - [`formData`] (Object)
    - [`mimeType`] (String)
3. [`hooks`] (Object)
    - `onProgress` (Function)
4. [`callback`] (Function)

#### 返回
1. `result` (Object)
    - `status` (Int)
    - `statusText` (String)
    - `ok` (Boolean) (status `2xx`)
    - `headers` (String)
    - `data` (String)

#### 示例
```js
Nat.upload('http://uploader.示例.com', {
    path: 'file:///tmp/intapp/nat/sample/localFile'
}, (err, ret) => {
    console.log(ret)
})
```

```js
Nat.upload('http://uploader.示例.com', {
    path: 'file:///tmp/intapp/nat/sample/localFile',
    method: 'PUT',
    formData: {
        framework: 'weex/nat'
    },
    headers: {
        'x-app': 'nat/0.0.8',
        'x-sign': 'bfbbf4c1f087d972'
    }
}, {
    onProgress: (p) => {
        console.log('Progressing: ' + p)
    }
}, (err, ret) => {
    console.log(ret)
})
```

---

> **Error**	
> DOWNLOAD_INTERNAL_ERROR	
> DOWNLOAD_INVALID_ARGUMENT	
> DOWNLOAD_NETWORK_ERROR	
> UPLOAD_INTERNAL_ERROR	
> UPLOAD_INVALID_ARGUMENT	
> UPLOAD_NETWORK_ERROR	

