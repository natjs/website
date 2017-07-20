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

// Make a phone call
Nat.call('415-736-0000')

// Take a photo
Nat.camera.captureImage((err, ret) => {
    console.log('Path: ', ret.path)
})

// Get device info
Nat.device.info((err, ret) => {
    console.log('Info: ', ret)
})

</script>

```

