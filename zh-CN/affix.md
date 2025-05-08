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

| 名称       | 说明                                                 | 类型                                                                               | 默认值 |
| -------- | -------------------------------------------------- | -------------------------------------------------------------------------------- | --- |
| 偏移量      | 偏移距离                                               | ^[number]                    | 0   |
| position | 固钉位置                                               | ^[enum]`'top' \\| 'bottom'` | top |
| target   | target container (CSS selector) | ^[string]                    | —   |
| z-index  | `z-index` of affix                                 | ^[number]                    | 100 |

### Events

| Name   | Description                       | Type                                                                                                                    |
| ------ | --------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| change | triggers when fixed state changed | ^[Function]`(fixed: boolean) => void`                               |
| scroll | triggers when scrolling           | ^[Function]`(value: { scrollTop: number, fixed: boolean }) => void` |

### Slots

| Name    | Description               |
| ------- | ------------------------- |
| default | customize default content |

### Exposes

| Name       | Description                 | Type                                                                        |
| ---------- | --------------------------- | --------------------------------------------------------------------------- |
| update     | update affix state manually | ^[Function]`() => void` |
| updateRoot | update rootRect info        | ^[Function]`() => void` |
