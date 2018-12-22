# taobao-top-client
淘宝联盟node sdk，因官方提供的版本已不可用，因此提供非官方版，希望比官方好用，欢迎issue和pr。

#### 安装
使用npm:
```
npm i taobao-top-client -S
```
或者yarn:
```
yarn add taobao-top-client
```

#### 引入文件
```
const { TopClient } = require('taobao-top-client')
```

#### 配置
使用淘宝联盟的appkey，appsecret和api的endpoint进行初始化:
```
klcps.config({
  appkey: 'yourappkey',
  appSecret: 'yourappsecret',
  url: 'taobao top endpoint', // 默认为 http://gw.api.taobao.com/router/rest
})
```

#### API
注意调用api返回的都是promise，可使用async/await；
