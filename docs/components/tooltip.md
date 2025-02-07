工具提示用于对指定元素进行补充文本提示、或提供上下文信息，以便更好地理解该元素的功能或作用。

## 使用方法 {#usage}

按需导入组件：

```js
import 'mdui/components/tooltip.js';
```

按需导入组件的 TypeScript 类型：

```ts
import type { Tooltip } from 'mdui/components/tooltip.js';
```

使用示例：

```html,example
<mdui-tooltip content="Plain tooltip">
  <mdui-button>button</mdui-button>
</mdui-tooltip>
```

## 示例 {#examples}

### 纯文本 tooltip {#example-plain}

默认为纯文本 tooltip。可通过 `content` 属性指定 tooltip 的内容。

```html,example,expandable
<mdui-tooltip content="Plain tooltip">
  <mdui-button>button</mdui-button>
</mdui-tooltip>
```

也可以通过 `content` slot 指定 tooltip 的内容。

```html,example,expandable
<mdui-tooltip>
  <mdui-button>button</mdui-button>
  <div slot="content">
    <div style="font-size: 1.4em">title</div>
    <div>content</div>
  </div>
</mdui-tooltip>
```

### 富文本 tooltip {#example-rich}

指定 `variant` 的值为 `rich`，即为富文本 tooltip。可通过 `headline` 属性指定 tooltip 的标题，`content` 属性指定 tooltip 的内容。

```html,example,expandable
<mdui-tooltip
  variant="rich"
  headline="Rich tooltip"
  content="Rich tooltips bring attention to a particular element of feature that warrants the user's focus. It supports multiple lines of informational text."
>
  <mdui-button>button</mdui-button>
</mdui-tooltip>
```

也可以通过 `headline`、`content` slot 指定 tooltip 的标题和内容。通过 `action` slot 指定 tooltip 的操作按钮。

```html,example,expandable
<mdui-tooltip variant="rich">
  <mdui-button>button</mdui-button>
  <div slot="headline">Rich tooltip</div>
  <div slot="content">Rich tooltips bring attention to a particular element of feature that warrants the user's focus. It supports multiple lines of informational text.</div>
  <mdui-button slot="action" variant="text">Action</mdui-button>
</mdui-tooltip>
```

### 位置 {#example-placement}

使用 `placement` 属性设置 tooltip 的位置。

```html,example,expandable
<div class="example-placement">
  <div class="row">
    <mdui-tooltip placement="top-left" content="top-left">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="top-start" content="top-start">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="top" content="top">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="top-end" content="top-end">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="top-right" content="top-right">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
  </div>
  <div class="row">
    <mdui-tooltip placement="left-start" content="left-start">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="right-start" content="right-start">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
  </div>
  <div class="row">
    <mdui-tooltip placement="left" content="left">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="right" content="right">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
  </div>
  <div class="row">
    <mdui-tooltip placement="left-end" content="left-end">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="right-end" content="right-end">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
  </div>
  <div class="row">
    <mdui-tooltip placement="bottom-left" content="bottom-left">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="bottom-start" content="bottom-start">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="bottom" content="bottom">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="bottom-end" content="bottom-end">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
    <mdui-tooltip placement="bottom-right" content="bottom-right">
      <mdui-card variant="outlined"></mdui-card>
    </mdui-tooltip>
  </div>
</div>

<style>
.example-placement mdui-card {
  width: 2.5rem;
  height: 2.5rem;
  margin: 0.25rem;
}

.example-placement .row:nth-child(2) mdui-tooltip:last-child mdui-card,
.example-placement .row:nth-child(3) mdui-tooltip:last-child mdui-card,
.example-placement .row:nth-child(4) mdui-tooltip:last-child mdui-card {
  margin-left: 10rem;
}
</style>
```

### 触发方式 {#example-trigger}

使用 `trigger` 属性设置 tooltip 的触发方式。

```html,example,expandable
<mdui-tooltip trigger="click" content="tooltip">
  <mdui-button>button</mdui-button>
</mdui-tooltip>
```

### 打开/关闭延时 {#example-delay}

在触发方式为鼠标悬浮触发时，可以使用 `open-delay` 属性设置打开延时，`close-delay` 属性设置关闭延时。单位为毫秒。

```html,example,expandable
<mdui-tooltip open-delay="1000" close-delay="1000" content="tooltip">
  <mdui-button>button</mdui-button>
</mdui-tooltip>
```

### 禁用状态 {#example-disabled}

添加 `disabled` 属性，可以禁用 tooltip。

```html,example,expandable
<mdui-tooltip disabled content="tooltip">
  <mdui-button>button</mdui-button>
</mdui-tooltip>
```
