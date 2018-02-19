# 通讯 / Communication

```bash
weexpack plugin add nat-communication
```

### call(to, callback) <span class="sub">拨打电话</span>

#### 参数
1. `to` (String)
2. [`callback`] (Function)

#### 示例
```js
Nat.call('415-736-0000')
```

```js
Nat.call('415-736-0000', () => {
    console.log('called')
})
```

---

### mail(to, options, callback) <span class="sub">发送邮件</span>

#### 参数
1. `to` (String | Array)
2. [`options`] (Object)
    - `subject` (String)
    - `body` (String)
3. [`callback`] (Function)

#### 示例
```js
Nat.mail('hi@natjs.com')
```

```js
Nat.mail(['hi@natjs.com', 'dev@natjs.com'], {
    subject: 'Subject',
    body: 'content goes here'
}, () => {
    console.log('email popup')
})
```

---

### sms(to, message, callback) <span class="sub">发送短信</span>

#### 参数
1. `to` (String | Array)
2. [`message`] (String)
3. [`callback`] (Function)

#### 示例
```js
Nat.sms('415-736-0000')
```

```js
Nat.sms(['415-736-0000', '425736-32'], 'message goes here', () => {
    console.log('sms popup')
})
```

---

> **Error**	
> CALL_PHONE_PERMISSION_DENIED	
> SEND_SMS_PERMISSION_DENIED	
> CALL_INVALID_ARGUMENT	
> SMS_INVALID_ARGUMENT	
> MAIL_INVALID_ARGUMENT	