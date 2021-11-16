# 前端项目注意事项

## 项目依赖
### [package.json](https://docs.npmjs.com/cli/v7/configuring-npm/package-json/)
每个项目的根目录下面，一般都有一个 package.json 文件，定义了这个项目所需要的各种模块，以及项目的配置信息（比如名称、版本、许可证等元数据）。npm install 命令根据这个配置文件，自动下载所需的模块，也就是配置项目所需的运行和开发环境。

``` json
{
  "dependencies": {
    "vue": "2.6.14",
    "react": "~17.0.2"
    "angular": "^13.0.1"
  },
  "devDependencies": {},
  "scripts": {
    "start": "...",
    "dev": "...",
    "watch": "...",
    "test": "...",
    "build": "...",
    "build:prod": "..."
  }
}
```

### [package-lock.json](https://docs.npmjs.com/cli/v7/configuring-npm/package-lock-json/) / [yarn.lock](https://classic.yarnpkg.com/en/docs/yarn-lock/)
该文件旨在跟踪被安装的每个软件包的确切版本，以便产品可以以相同的方式被 100％ 复制（即使软件包的维护者更新了软件包）。package-lock.json 会固化当前安装的每个软件包的版本，当运行 npm install 时，npm 会使用这些确切的版本。package-lock.json 文件需要被提交到 Git 仓库，以便被其他人获取（如果项目是公开的或有合作者，或者将 Git 作为部署源）。

## [代码格式化](https://lexiangla.com/docs/5a52b0dc0bc211ec9c20d2f844567384?company_from=385abcf0dd9d11e8a11752540005f435)[【备用链接】](https://github.com/297087852/docs/tree/main)
***关闭编辑器的代码格式化功能！***

### [ESLint](https://eslint.org/)[【ESLint 规则】](https://cn.eslint.org/docs/rules/)
JS 语法规则和代码风格的检查工具，可以用来保证写出语法正确、风格统一的代码。

### 规则
1. [Standard](https://standardjs.com/rules-zhcn.html)
2. [Airbnb](https://lin-123.github.io/javascript/)
3. [Google](https://google.github.io/styleguide/jsguide.html)

### 要求
1. 不允许将带有 ESLint 报错的代码提交到远程

### [.editorconfig](https://editorconfig.org/)
帮助开发人员在不同的编辑器和 IDE 之间定义和维护一致的编码样式。

```
root = true

[*]
indent_style = space
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
```

### 其它
1. [Prettier](https://prettier.io/)
2. [Stylelint](https://stylelint.io/)
3. [commitlint](https://commitlint.js.org/)

## 环境变量
1. 接口地址等变量不可以硬编码在项目中，建议使用环境变量作区分。
2. 调试数据尽量使用环境变量定义以确保调试被限制在特定环境里

## console.log
1. 临时调试，用完删除。
2. 可用于重要模块的日志打印
