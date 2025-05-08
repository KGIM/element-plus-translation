---
title: 提示
lang: en-US
---

# 提示

用于页面中展示重要的提示信息。

## 基础用法

Alert 组件不属于浮层元素，不会自动消失或关闭。

:::demo Alert 组件提供四种类型，由 type 属性指定，默认值为 info。

提示/基础用法

:::

## 主题

提示提供两个不同的主题，`light`和`dark`。

:::demo 设置 `effect` 以更改主题，默认值是 `light` 。

提示/主题

:::

## 自定义关闭按钮

Customize the close button as texts or other symbols.

:::demo Alert allows you to configure if it's closable. The close button text and closing callbacks are also customizable. `closable` attribute decides if the component can be closed or not. It accepts `boolean`, and the default is `true`. You can set `close-text` attribute to replace the default cross symbol as the close button. Be careful that `close-text` must be a string. `close` event fires when the component is closed.

alert/close-button

:::

## With Icon

Displaying an icon improves readability.

:::demo Setting the `show-icon` attribute displays an icon that corresponds with the current Alert type. Or use the `icon` slot to customize icon.

alert/icon

:::

## Centered Text

Use the `center` attribute to center the text.

:::demo

alert/center

:::

## With Description

Description includes a message with more detailed information.

:::demo Besides the required `title` attribute, you can add a `description` attribute to help you describe the alert with more details. Description can only store text string, and it will word wrap automatically.

alert/description

:::

## With Icon and Description

:::demo At last, this is an example with both icon and description.

alert/icon-description

:::

## Alert API

### Attributes

| Name        | Description                                              | Type                                                                                                            | Default |
| ----------- | -------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ------- |
| title       | alert title.                             | ^[string]                                                   | —       |
| type        | alert type.                              | ^[enum]`'success' \\| 'warning' \\| 'info' \\| 'error' ` | info    |
| description | descriptive text.                        | ^[string]                                                   | —       |
| closable    | whether alert can be dismissed.          | ^[boolean]                                                  | true    |
| center      | whether content is placed in the center. | ^[boolean]                                                  | false   |
| close-text  | customized close button text.            | ^[string]                                                   | —       |
| show-icon   | whether a type icon is displayed.        | ^[boolean]                                                  | false   |
| effect      | theme style.                             | ^[enum]`'light' \\| 'dark'`                                | light   |

### Events

| Name  | Description                                   | Type                                                                                         |
| ----- | --------------------------------------------- | -------------------------------------------------------------------------------------------- |
| close | trigger when alert is closed. | ^[Function]`(event: MouseEvent) => void` |

### Slots

| Name                                                             | Description                                       |
| ---------------------------------------------------------------- | ------------------------------------------------- |
| default                                                          | content of the alert description. |
| title                                                            | content of the alert title.       |
| icon ^(2.9.7) | content of the alert icon.        |
