# antd-img-crop

[![npm](https://img.shields.io/npm/v/antd-img-crop.svg?style=flat-square)](https://www.npmjs.com/package/antd-img-crop)

[English](./README.md) | 简体中文

图片裁切工具，用于 Ant Design [Upload](https://ant.design/components/upload-cn/) 组件。

## 示例

[https://codesandbox.io/s/4qoom5p9x4](https://codesandbox.io/s/4qoom5p9x4)

## 安装

```bash
yarn add antd-img-crop
```

## 使用

```jsx harmony
import ImgCrop from 'antd-img-crop';
import { Upload } from 'antd';

const Demo = () => (
  <ImgCrop>
    <Upload>+ Add image</Upload>
  </ImgCrop>
);
```

## Props

### width

类型：`number`，默认：`100`

裁切宽度，单位 `px`。若 `useRatio` 为 `true`，则是比例。

### height

类型：`number`，默认：`100`

裁切高度，单位 `px`。若 `useRatio` 为 `true`，则是比例。

### useRatio

类型：`boolean`，默认：`false`

是否将 `width` 和 `height` 用作比例，而非真实 `px`。此时裁切将占满宽度或高度。

例如，`width={500} height={400}` 与 `width={5} height={4}` 其实是一样的。

### resize

类型：`boolean`，默认：`true`

裁切是否可调整大小。

### resizeAndDrag

类型：`boolean`，默认：`true`

裁切是否可调整大小、可拖动。

### modalTitle

类型：`string`，默认：`"编辑图片"`

弹窗标题。

### modalWidth

类型：`number`，默认：`520`

弹窗宽度，单位 `px`。

### beforeCrop

类型：`function`，默认：-

图片裁切前执行，若返回 `false`，弹框将不会打开。（不支持 `Promise`）

Ant Design Upload 组件的 `beforeUpload` 属性在图片裁切后、上传前执行。

---
