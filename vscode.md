# vscode插件

- 插件名称
```bash
# 显示中文
Chinese（Simplified）(简体中文)Language Pack for Visual Studio Code
Django


# 统一代码风格，.editorconfig
EditorConfig for VS Code
# 如果未指定 root = true，则 EditorConfig 将继续在项目外部查找 .editorconfig 文件。
root = true
# 设置文件字符集
charset = utf-8
# 以下配置适用文件类型，可对不同文件类型设置不同规则
[*.{js,jsx,ts,tsx,vue,scss,json}]
# 保存时将换行符转换为 LF
end_of_line = lf
# 缩进格式
indent_style = space
indent_size = 2
# 保存时自动删除行尾的空白字符
trim_trailing_whitespace = true
# 保存时在文件末尾插入空白行
insert_final_newline = true


ES7 React/Redux/GraphQL/React-Nactive snippets

GitHub Theme
# git信息可视化，在代码里显示
GitLens - Git supercharged
# 查看git提交日志
Git History
Jupyter Notebook Renderers
Python
Python Environment Manager
Pylance
Jupyter
Settings Sync
# the tree view 中的文件名旁添加图标
vscode-icons
# 自动合闭html标签
Auto Close Tag 
Auto Complete Tag 
Auto Rename Tag
# 自动引入
Auto Import - ES6, TS, JSX, TSX
# 代码格式化
Prettier
# 括号成对检测,用颜色来标识匹配的括号
Bracket Pair Colorizer 2
# Vue必备，语法高亮，代码片段，自动补全，格式化代码
Vetur vue
# 检测英文单词拼写
Code Spell Checker
# 汇集常用正则
any-rule
# 自动补全代码中的路径和文件名
Path Intellisense
# 风格化在你的文件中找到的 css/web 颜色
Color Highlight
# 背景图片
background
# 注释美化
Better Comments 
"better-comments.tags": [
    {
        "tag": "fix",                     // 关键字（不区分大小写），Better Comments 检测到关键字后才会将这行注释转换样式
        "color": "#FF2D00",               // 文字颜色
        "strikethrough": false,           // 是否显示删除线
        "underline": false,               // 是否显示下划线
        "backgroundColor": "transparent", // 背景颜色
        "bold": false,                    // 是否加粗
        "italic": false                   // 是否启用斜体文字
    },
    ...多个关键字配置
]
# 显示文件大小
filezise
# 缩进高亮
indent-rainbow
{
    // 高亮颜色
    "indentRainbow.colors": [
        "rgba(40,140,160,0.3)",
        "rgba(40,160,140,0.3)",
        "rgba(60,140,140,0.3)",
        "rgba(60,160,160,0.3)"
    ],
    // tabSize 错误时的高亮颜色
    "indentRainbow.errorColor": "rgba(128,32,32,0.6)",
    // 混用空格和 tab 缩进时的高亮颜色
    "indentRainbow.tabmixColor": "rgba(128,32,96,0.6)",
    // 需要高亮显示的文件类型
    "indentRainbow.includedLanguages": [
        "vue",
        "html"
    ],
}
# 文件图标
Material Icon Theme 
# 基于 ElementUI 的自动补全插件
vscode-element-helper

# 代码格式检查工具，npm install -g eslint， .eslintrc.js
ESLint
module.exports = {
  env: {
    browser: true,
    commonjs: true,
    es6: true,
    node: true
  },
  extends: [
    'standard'
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly'
  },
  parserOptions: {
    ecmaVersion: 11
  },
  rules: { }
}

# 提供语法高亮，自动补全，文档提示，颜色选择，URL 跳转，ID 快速修改，SVG 预览与导出 PNG
SVG

# CSS 自动排序，在settings.json中添加配置：
CSScomb
{
    "csscomb.formatOnSave": true, // 保存时自动格式化
    "csscomb.preset": "csscomb" // 格式化模板
}

# JS 代码重构，editor.action.quickFix
 avaScript Booster

#  jsdoc 注释，文件 - 首选项 - 键盘快捷方式 - 搜索extension.genJSDoc，配置
jsdoc
# jsdoc 预览
Preview JSDOC

# 接口测试
REST Client 

```
<!-- https://juejin.cn/post/6856695988518993927 -->