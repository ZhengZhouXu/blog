### 调试
1. vscode 配置
安装vscode插件 Debugger for Chrome  
创建launch.json，配置如下
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Chrome",
      "type": "chrome",
      "request": "launch",
      "url": "http://localhost:3000",
      "webRoot": "${workspaceRoot}/src",
      "sourceMapPathOverrides": {
        "webpack:///src/*": "${webRoot}/*"
      }
    }
  ]
}
```

2.组件调试 [storybook](https://github.com/storybooks/storybook) 和 [React Styleguidist](https://react-styleguidist.js.org/)

3.打包分析
> npm install --save source-map-explorer
```json
"scripts": {
  "analyze": "source-map-explorer build/static/js/main.*",
}
```
>npm run build  
npm run analyze
