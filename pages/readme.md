# 页面目录

`Nuxt` 提供了基于文件的路由功能，用于在 `web` 应用中创建路由。

> 注：
> 为了减少文件包大小，此目录是可选的，即若只是用 App.vue，vue-router 将不会被包含在内。
> 若要强制使用页面系统，请在 `nuxt.config` 中设置 `pages: true`，或者在 `app/router/options.ts` 中设置。

## 使用方法

页面是 `Vue` 文件，可以使用 `Nuxt` 支持的任何扩展名。

`Nuxt` 会自动为 `~/pages` 目录中的每个页面创建一个路由。

路径为 `pages/index.vue` 的文件将映射到应用程序的 `/` 路由。

若使用 `App.vue`，需确保使用 `<NuxtPage />` 组件以显示当前页面。

```html
// app.vue
<template>
  <div>
    <!-- 所有页面共享的标记，例如导航栏 -->
    <NuxtPage />
  </div>
</template>
```

> 注意：
> 为保证页面之间的路由过渡，页面必须仅有一个单一的根元素。（HTML）注释也被视为根元素。

```html
// right
<template>
  <div>
    <!-- 此页面正确地只有一个单一根元素 -->
    页面内容
  </div>
</template>

// wrong
<template>
  <!-- 由于存在这个注释，该页面在路由更改期间的客户端导航时不会被渲染 -->
  <div>页面内容</div>
</template>

// wrong
<template>
  <div>此页面</div>
  <div>有多个根元素</div>
  <div>并且在路由更改期间的客户端导航时不会被渲染</div>
</template>
```

## 动态路由

## 全匹配路由

## 嵌套路由

## 页面元数据

## 导航

## 编程式导航

## 自定义路由

## 多个页面目录