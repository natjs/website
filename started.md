## Quick start

### Install

```bash
npm install natjs --save
```

### Add modules you need

```bash
weexpack plugin add [nat moudle]
```

### Usage

Import `natjs` in weex file (.we/.vue)

```vue
<script>
import Nat from 'natjs'

// make a phone call
Nat.call('415-736-0000')

// take a photo
Nat.camera.captureImage((err, ret) => {
    console.log('Path: ', ret.path)
})

</script>

```

