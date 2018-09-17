# n22-postcss-px2rem

基于postcss-px2rem进行二次开发，增加第三方UI排除方法

## package.json配置(表达式字符串)
```
"postcss": {
  "plugins": {
    "autoprefixer": {},
    "px2rem-exclude": {
      "remUnit": 75,
      "exclude": "node_modules|otherFolder"
    }
  }
}
```

## .postcssrc.js(正则表达式)
```
module.exports = {
  'plugins': {
    'px2rem-exclude': {
      remUnit: 75,
      exclude: /node_modules|otherFolder/i
    }
  }
}
```
----
单独样式无需转换可以使用**Px**、**PX**或/* no */注释
```
.demo{
  font-size:14Px;
  height:100Px;
  width:100px; /* no */
}
```