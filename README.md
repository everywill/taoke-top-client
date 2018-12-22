# taoke-top-client
淘宝联盟node sdk，因官方提供的版本已不可用，因此提供非官方版，希望比官方好用，欢迎issue和pr。

#### 安装
使用npm:
```
npm i taoke-top-client -S
```
或者yarn:
```
yarn add taoke-top-client
```

#### 引入文件
```
const { TopClient } = require('taoke-top-client')
```

#### 配置
使用淘宝联盟的appkey，appsecret和api的endpoint进行初始化:
```
const client = new TopClient({
  appkey: 'yourappkey',
  appSecret: 'yourappsecret',
  url: 'taobao top endpoint', // 默认为 http://gw.api.taobao.com/router/rest
})
```

#### API
例如查询商品： 
```
client.execute('taobao.tbk.item.get', {
      fields: 'num_iid,title,pict_url,small_images,reserve_price,zk_final_price,user_type,item_url,volume',
      q: '逆水寒',
      sort: 'tk_total_sales_des,
      page_no: 1,
      page_size: 2,
    })
```
注意调用api返回的都是promise，因此可使用async/await。
