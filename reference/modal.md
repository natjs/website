# Modal

```bash
weexpack plugin add nat-modal
```

### alert(options, callback)

#### Arguments
1. `message`|`options` (String | Object)
	- `title` (String)
	- `message` (String)
	- `okButton` (String) (default: `OK`)
2. [`callback`] (Function)

#### Example
```js
Nat.alert('What\'s up')
```

```js
Nat.alert({
	title: 'Title',
	message: 'This is an alert dialog',
	okButton: 'I know'
}, () => {
	console.log('alerted')
})
```

---

### confirm(options, callback)

#### Arguments
1. `message`|`options` (String | Object)
	- `title` (String)
	- `message` (String)
	- `okButton` (String) (default: `OK`)
	- `cancelButton` (String) (default: `Cancel`)
2. [`callback`] (Function)

#### Returns
1. `result` (Boolean)

#### Example
```js
Nat.confirm('Are you okay?')
```

```js
Nat.confirm({
	title: 'Title',
	message: 'Are you okay?',
	okButton: 'I\'m OK',
	cancelButton: 'Not OK'
}, (err, ret) => {
	console.log((ret) ? 'confirmed' : 'canceled')
})
```

---

### prompt(options, callback)

#### Arguments
1. `message`|`options` (String | Object)
	- `title` (String)
	- `message` (String)
	- `text` (String)
	- `okButton` (String) (default: `OK`)
	- `cancelButton` (String) (default: `Cancel`)
2. [`callback`] (Function)

#### Returns
1. `result` (Object)
	- result (Boolean)
	- data (String)

#### Example
```js
Nat.prompt('Are you feeling lucky?')
```

```js
Nat.prompt({
	title: 'Title',
	message: 'Are you feeling lucky?',
	text: 'sure',
	okButton: 'Yep',
	cancelButton: 'Ignore'
}, (err, ret) => {
	console.log((ret.result) ? ret.data : 'canceled')
})
```

---

### toast(options)

#### Arguments
1. `message`|`options` (String | Object)
	- `message` (String)
	- `duration` (Int) (ms)
	- `postion` (String) (`top` | `middle` | `bottom`, default: `bottom`)

#### Example
```js
Nat.toast('What\'s up')
```

```js
Nat.toast({
	message: 'What\'s up up',
	duration: 5000,
	postion: 'top'
})
```

---

> **Error**	
> ALERT_INVALID_ARGUMENT	
> CONFIRM_INVALID_ARGUMENT	
> PROMPT_INVALID_ARGUMENT	
> TOAST_INVALID_ARGUMENT	
