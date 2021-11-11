# 前端代码最佳实践

## JS
### if 条件判断
``` js
if (a === true) {
  doSomething()
}

// 类似的
const b = condition ? true : false
```

建议
``` js
if (a) {
  doSomething()
}

const b = Boolean(condition)
const b = !!condition
```

### if 条件判断 2
``` js
if (a == 1) {
  doThis()
} else if (a == 2) {
  doThat()
} else if (a == 3) {
  doWhatever()
}
```

建议
``` js
switch (a) {
  case 1:
    doThis()
    break
  case 2:
    doThat()
    break
  case 3:
    doWhatever()
}
```

### if 条件判断 3
``` js
let a
if (condition) {
  a = 1
} else {
  a = 0
}
```

建议
``` js
const a = condition ? 1 : 0
```

### 复杂类型的引用传值
``` js
const a = {x: 1}
const b = a
b.x = 2
console.log(a)
```

建议
``` js
const b = JSON.parse(JSON.stringify(a))
```

## React
1. [React Hook](https://lexiangla.com/docs/3babd20e0bd011ec9abb6e2d8f959e52?company_from=385abcf0dd9d11e8a11752540005f435)
2. [React关于shouldComponentUpdate、PureComponent和React.memo](https://lexiangla.com/docs/4136d1300bd811ecb0be32c75543b97e?company_from=385abcf0dd9d11e8a11752540005f435)

## Vue
1. [vue之keep-alive的应用](https://lexiangla.com/docs/5672c9420bd211ec9efa762d8987966a?company_from=385abcf0dd9d11e8a11752540005f435)

## 通用
### 组件、代码复用
1. 能复用尽量复用，避免重复造轮子
2. 公共模块尽量提取出来

### 数据和模板分离
1. 多个相同的 HTML 结构尽量使用数据循环输出模板内容
