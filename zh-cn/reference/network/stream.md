# 网络请求 / Stream

```bash
weexpack plugin add nat-stream
```

### fetch(url, options, callback) <span class="sub">Fetch</span>

#### 参数
1. `url` (String)
2. [`options`] (Object)
	- `method` (String) (`GET` | `POST` | `PUT` | `PATCH` | `DELETE` | `HEAD`, default: `GET`)
	- `headers` (Object)
	- `type` (String) (`json` | `jsonp` | `text`, default: `json`)
	- `body` (String)
2. [`callback`] (Function)

#### 返回
1. `result` (Object)
	- `status` (Int)
	- `statusText` (String)
	- `ok` (Boolean) (status `2xx`)
	- `headers` (String)
	- `data` (String)

#### 示例
```js
Nat.fetch('https://suggest.taobao.com/sug?q=htc', (err, ret) => {
	console.log(ret)
})
```

```js
Nat.fetch('https://suggest.taobao.com/sug?q=htc', {
	method: 'GET',
	headers: {
		'x-app': 'nat/0.0.8',
		'x-sign': 'bfbbf4c1f087d972'
	},
	type: 'json'
}, (err, ret) => {
	console.log(ret)
})
```

---

> **Error**	
> FETCH_INTERNAL_ERROR	
> FETCH_INVALID_ARGUMENT	
> FETCH_NETWORK_ERROR	

