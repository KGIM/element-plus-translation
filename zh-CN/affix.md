---
title: 固钉
lang: en-US
---

# 固钉

将页面元素固定在特定可视区域。

## 基础用法

固钉默认固定在页面顶部。

:::demo 通过设置 offset 属性来改变吸顶距离，默认值为 0。

affix/basic

:::

## Target Container

You can set `target` attribute to keep the affix in the container at all times. It will be hidden if out of range.

:::demo Please notice that the container avoid having scrollbar.

affix/target

:::

## Fixed Position

The affix component provides two fixed positions: `top` and `bottom`.

:::demo 您可以设置 `position` 属性来更改固定位置，默认值是 `top` 。

affix/fixed

:::

## API

### 属性

| 名称       | 说明                                | 类型                                                                          | 默认值 |
| -------- | --------------------------------- | --------------------------------------------------------------------------- | --- |
| 偏移量      | 偏移距离                              | ^[number]               | 0   |
| position | 固钉位置                              | ^[enum]\`top' \\| '底部' | top |
| target   | 目标容器 (CSS 选择器) | ^[string]               | —   |
| z-index  | `z-index` of affix                | ^[number]               | 100 |

### 事件

| 名称     | 描述           | 类型                                                                                                                      |
| ------ | ------------ | ----------------------------------------------------------------------------------------------------------------------- |
| change | 固钉状态改变时触发的事件 | ^[Function]`(fixed: boolean) => void`                               |
| scroll | 滚动时触发的事件     | ^[Function]`(value: { scrollTop: number, fixed: boolean }) => void` |

### 插槽

| 名称  | 描述      |
| --- | ------- |
| 默认值 | 自定义默认内容 |

### 暴露

| 名称         | 描述           | 类型                                                                          |
| ---------- | ------------ | --------------------------------------------------------------------------- |
| 更新         | 手动更新固钉状态     | ^[Function]`() => void` |
| updateRoot | 手动更新根元素的模型信息 | ^[Function]`() => void` |
