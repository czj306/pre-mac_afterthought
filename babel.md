# Babel 入门教程

Babel是一个广泛使用的转码器，可以将ES6代码转为ES5代码，从而在现有环境执行。

## 例子

``` js
// 转码前
input.map(item => item + 1);
// 转码后
input.map(function (item) { 
    return item + 1
});
```

## 配置文件 .babelrc

Babel的配置文件是` .babelrc`，存放在项目的根目录。

``` bash
{
    "presets": [],
    "plugins": []
}
```

### `presets` 字段设定转码规则

``` bash
# ES2015转码规则
npm install --save-dev babel-preset-es2015
# react转码规则
npm install --save-dev babel-preset-react
# ES7不同阶段语法提案的转码规则（共有4个阶段），选装一个
npm install --save-dev babel-preset-stage-0
npm install --save-dev babel-preset-stage-1
npm install --save-dev babel-preset-stage-2
npm install --save-dev babel-preset-stage-3
```

### 增加规则到`.babelrc`

```bash
{
	"presets": [
		"es2015",
		"react",
		"stage-2"
	],
	"plugins": []
}
```



## 转码命令行

Babel提供`babel-cli`工具，用于命令行转码。

``` bash
- npm install --global babel-cli

# 转码结果输出到标准输出
$ babel example.js

# 转码结果写入一个文件
# --out-file 或 -o 参数指定输出文件
$ babel example.js --out-file compiled.js
# 或者
$ babel example.js -o compiled.js

# 整个目录转码
# --out-dir 或 -d 参数指定输出目录
$ babel src --out-dir lib
# 或者
$ babel src -d lib

# -s 参数生成source map文件
$ babel src -d lib -s
```

