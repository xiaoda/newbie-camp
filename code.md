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
} else {
  doNothing()
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
    break
  default:
    doNothing()
}
```

### if 条件判断 3
``` js
let a
if (condition) {
  a = 1
} else {
  a = 2
}
```

建议
``` js
const a = condition ? 1 : 2
```

### if 条件判断 4
``` js
if (!a) {
  if (b) {
    if (!c) {
      doThis()
    } else {
      doThat()
    }
  } else {
    doWhatever()
  }
} else {
  doNothing()
}
```

建议
``` js
if (a) {
  doNothing()
} else {
  if (b) {
    if (c) {
      doThat()
    } else {
      doThis()
    }
  } else {
    doWhatever()
  }
}
```

### indexOf
``` js
const stringContainX = a.indexOf('x')
const arrayContainX = b.indexOf('y')
```

建议
``` js
const stringContainX = a.includes('x')
const stringContainX = a.startsWith('x')
const stringContainX = a.endsWith('x')
const arrayContainX = b.includes('y')
```

### 数组方法的选择
``` js
const a = array.forEach(...)
array.map(...)
```

建议
``` js
array.forEach(...)
const b = array.map(...)
```

### 删除数组元素
``` js
array.forEach((item, index) => {
  if (index % 2 === 0) {
    array.splice(index, 1)
  }
})
```

### 复杂类型的引用传值
``` js
const a = {x: 1}
const b = a
b.x = 2
console.log(a.x)
```

建议
``` js
// 深度克隆
const b = JSON.parse(JSON.stringify(a))
```

### 运行时报错：对象为空
*Can not read property x of undefined*
``` js
const b = a.x
```

建议
``` js
const b = a ? a.x : null

// or
const b = a?.x
```

## React
1. [React Hook](https://lexiangla.com/docs/3babd20e0bd011ec9abb6e2d8f959e52?company_from=385abcf0dd9d11e8a11752540005f435)[【备用链接】](https://github.com/TwoNingMengTea/reack-hook/blob/master/react-hooks.md)
2. [React关于shouldComponentUpdate、PureComponent和React.memo](https://lexiangla.com/docs/4136d1300bd811ecb0be32c75543b97e?company_from=385abcf0dd9d11e8a11752540005f435)

## Vue
1. [vue之keep-alive的应用](https://lexiangla.com/docs/5672c9420bd211ec9efa762d8987966a?company_from=385abcf0dd9d11e8a11752540005f435)

## 综合
### 组件、代码复用
1. 能复用尽量复用，避免重复造轮子
2. 可以复用的模块、组件、方法等尽量提取出来
3. 公共代码是可以修改的，但要谨慎考虑各种情况。

### 数据和模板分离
1. 多个相同或类似的 HTML 结构尽量使用数据循环输出模板内容

### 问题解决
1. 遇到问题先自行思考或搜索
2. 比报错更重要的是具体的错误信息
3. 一段时间内无法解决的问题及时向组长/主管求助
4. 不要用猥琐的方式（奇巧淫技）解决问题

### 代码可读性
1. 代码可读性在某种程度上比代码运行效率更重要，为了可读性降低一点效率是可以接受的。
2. 对代码进行必要的注释，特别是核心模块、公共组件、通用方法、重要参数等。

## 参考资料
1. [编码规范 by @mdo](https://codeguide.bootcss.com/)
2. [ES6 入门教程 by 阮一峰](https://es6.ruanyifeng.com/)
3. [Javascript 秘密花园](http://bonsaiden.github.io/JavaScript-Garden/zh/)
