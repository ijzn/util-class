使用文档

```
npm i -D utils-class

import { getIn } from 'utils-class'
cosnt person = {
 name: {
  newName: 'sun',
  oldName: 'flover'
 },
 childre: [{
  name: 'zhangsan'
 },{
  name: 'lisi'
 }]
}

getIn(person, ['name','newName'], '') // 'sun'
getIn(person, ['childre', 0, 'name'], '') // zhangsan
getIn(person, ['sex'], '默认值') // 默认值

```

## manipulate 防空处理

|  函数名  |                          说明                          |
| :------: | :----------------------------------------------------: |
|  getIn   |  从一个对象通过操作序列来拿里面的值，做了基本防空措施  |
|          |        @param {object} state - 需要获取的数据源        |
|          |            @param {array} array - 操作路径             |
|          |    @param {any} initial - 默认值，当没有内容的时候     |
|  setIn   |   一个对象通过操作序列来设置里面的值，做到自动添加值   |
|          |        @param {object} state - 需要获取的数据源        |
|          |            @param {array} array - 操作路径             |
|          |    @param {any} initial - 默认值，当没有内容的时候     |
| deleteIn | 一个对象通过操作序列来删除里面的值, 做到防空, 返回新值 |
|          |        @param {object} state - 需要获取的数据源        |
|          |            @param {array} array - 操作路径             |
| compose  |        将一组操作通过 array 的形式 reduce 组合         |
|          |            @param {array} array - 组合方式             |

## 常用数据类型判断

| 函数名       |            说明            |
| ------------ | :------------------------: |
| isArray      |   判断是否是 array 类型    |
| isArray      |   判断是否是 array 类型    |
| isObject     |   判断是否为 object 对象   |
| isString     |     判断是否为 string      |
| isPromise    |     判断是否为 promise     |
| isSymbol     |     判断是否是 symbol      |
| isFunc       |       判断是否是函数       |
| canParseJson |        能否 json 化        |
| isTelNum     | 判断是否符合手机号格式标准 |

## 常用设备的系统判断, android or ios

|                     函数名 ｜ 说明                     |
| :----------------------------------------------------: |
|   isIOS ｜判断是否是 IOS 返回值 Boolean (true/false)   |
| isAndroid ｜判断是否是安卓 返回值 Boolean (true/false) |

## Object 序列化

buildQueryString 编译成 url
