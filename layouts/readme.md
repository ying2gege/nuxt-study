# 通用布局目录

`Nuxt` 提供了一个布局框架，用于将常见的 `UI` 模式提取为可重用的布局。

> 注：
> 为了获取最佳性能，在使用时，放置在此目录中的组件将通过异步导入自动加载。

## 启用布局

通过在 `App.vue` 中添加 `<NuxtLayout />` 启用。

```vue [App.vue]
<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
```

可采用以下两种方式使用布局：

- 在页面中使用 `definePageMeta` 设置 `layout` 属性。
- 设置 `<NuxtLayout />` 的 `name` 属性。

> 注：
> 布局名称会被规范化为 `kebab-case`(短横线连接)，即 `someLayout` 将变为 `some-layout`。

> 注：
> 若没有指定布局，将使用 `layouts/default.vue`。

> 注：
> 若程序只有一个布局，建议使用 `App.vue`。

> 注：
> 布局必须具有单个根元素，以允许 `Nuxt` 在布局更改时应用过渡效果，而且根元素不能是 `<slot />`。

## 默认布局

## 命名布局

## 动态更改布局

## 在每个页面上覆盖布局
