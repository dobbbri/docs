---
title: "API:globalName 属性"
description: Nuxt.js允许您自定义主HTML模板中使用的全局ID以及主Vue实例名称和其他选项。
---

# globalName 属性

> Nuxt.js允许您自定义主HTML模板中使用的全局ID以及主Vue实例名称和其他选项。

- 类型: `Object`
- 默认: `nuxt`

例子:

`nuxt.config.js`

```js
{
  globalName: 'myCustomName'
}
```

它必须是有效的JavaScript标识符。

## globals 属性

> 自定义默认情况下基于`globalName`的特定全局名称。

- 类型: `Object`
- 默认:

```js
{
  id: globalName => `__${globalName}`,
  nuxt: globalName => `$${globalName}`,
  context: globalName => `__${globalName.toUpperCase()}__`,
  pluginPrefix: globalName => globalName,
  readyCallback: globalName => `on${_.capitalize(globalName)}Ready`,
  loadedCallback: globalName => `_on${_.capitalize(globalName)}Loaded`
},
```

