# Image

```bash
weexpack plugin add nat-media-image
```

### pick(options, callback)

#### Arguments
1. `options` (Object)
	- `limit` (Int) (default: `1`)
	- `quality` (Int) (default: `100`)
	- `width` (Int)
	- `height` (Int)
	- `showCamera` (Boolean) (default: `false`)
2. [`callback`] (function)

#### Returns
1. `result` (Object)
	- `paths` (Array)

#### Example
```js
Nat.image.pick({
	limit: 3,
	showCamera: false
}, (err, ret) => {
	console.log(ret.paths)
})
```

---

### preview(urls, options, callback)

#### Arguments
1. `urls` (String|Array)
2. [`options`] (Object)
	- `current` (Int) (index)
	- `style` (String) (`dots` | `label` | `none`, default: `dots`)
3. [`callback`] (function)

#### Example
```js
Nat.image.preview('http://cdn.instapp.io/nat/samples/01.jpeg')
```

```js
Nat.image.preview([
	'http://cdn.instapp.io/nat/samples/01.jpeg',
	'http://cdn.instapp.io/nat/samples/02.jpeg'
], {
	current: 1,
	style: 'none'
})
```

---

### info(url, callback)

#### Arguments
1. `url` (String)
2. [`callback`] (function)

#### Returns
1. `result` (Object)
	- `width` (Int)
	- `height` (Int)

#### Example
```js
Nat.image.info('http://cdn.instapp.io/nat/samples/01.jpeg', (err, ret) => {
	console.log(ret)
})
```

---

### exif(url, callback)

#### Arguments
1. `url` (String)
2. [`callback`] (function)

#### Returns
1. `result` (Object) ([Exif Info](http://www.cipa.jp/std/documents/e/DC-008-2012_E.pdf))

#### Example
```js
Nat.image.exif('http://cdn.instapp.io/nat/samples/01.jpeg', (err, ret) => {
	console.log(ret)
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
