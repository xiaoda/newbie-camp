# 前端项目注意事项

## 项目依赖
### package.json
每个项目的根目录下面，一般都有一个package.json文件，定义了这个项目所需要的各种模块，以及项目的配置信息（比如名称、版本、许可证等元数据）。npm install命令根据这个配置文件，自动下载所需的模块，也就是配置项目所需的运行和开发环境。

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

### package-lock.json / yarn-lock.json
该文件旨在跟踪被安装的每个软件包的确切版本，以便产品可以以相同的方式被 100％ 复制（即使软件包的维护者更新了软件包）。package-lock.json 会固化当前安装的每个软件包的版本，当运行 npm install时，npm 会使用这些确切的版本。package-lock.json 文件需要被提交到 Git 仓库，以便被其他人获取（如果项目是公开的或有合作者，或者将 Git 作为部署源）。

## 代码格式化
### [ESLint](https://eslint.org/)
JS 语法规则和代码风格的检查工具，可以用来保证写出语法正确、风格统一的代码。

[【所有规则】](https://eslint.bootcss.com/docs/rules/)

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

## 调试
### console.log
1. 临时调试，用完清除。
2. 可用于重要模块的日志打印
