## 快速开始


### 初始化 Weex 项目

```bash
weexpack create [project name]
```

### 进入项目目录

```bash
cd [project name]
```

### 安装 nat.js

```bash
npm install natjs --save
```

### 按需引入模块

```bash
weexpack plugin add [nat moudle]
...
```

### 开始使用

在 vue/weex 文件中使用 Nat (`.vue`/`.we`)

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
