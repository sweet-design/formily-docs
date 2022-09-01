---
title: 输入组件
order: 2
toc: menu
---

# 输入组件

一般出现在需要用户提交信息或者收集用户信息的场景，目前 formily 支持一下基础输入组件：

## 输入框

通过鼠标或键盘输入内容，是最基础的表单域的包装。

### 使用场景

- 需要用户输入表单域内容时
- 提供组合型输入框，带搜索的输入框，还可以进行大小选择

### cate

- 类别：字段属性
- 名称：控件类别
- 类型: `string`
- 默认值：`'input'`
- 详细：

控件的类别。

### type

- 类别：字段属性
- 名称：控件类型
- 类型: `string`
- 默认值：`'input'`
- 详细：

控件的类型。

### name

- 类别：字段属性
- 名称：字段标识
- 类型: `string`
- 默认值：`''`
- 详细：

一般指对应数据库中的列名,只能用英文字母。

示例：

```js
{
  name: 'name';
}
```

### title

- 类别：字段属性
- 名称：标题
- 类型: `string`
- 默认值：`'输入框'`
- 详细：

指显示控件的名称，如果配置了国际化标识，将读取指定的数据，否则此处将作为默认值。

示例：

```js
{
  title: '姓名';
}
```

### titleLangKey

- 类别：字段属性
- 名称：标题国际化标识
- 类型：`string`
- 默认值：`''`
- 详细：

指多语言对应的 key，不限制标识格式。

示例：

```js
{
  titleLangKey: 'name';
}
```

### description

- 类别：字段属性
- 名称：描述
- 类型：`string`
- 默认值：`''`
- 详细：

指给字段进行简单描述或者备注。

示例：

```js
{
  description: '名称';
}
```

### descriptionLangKey

- 类别：字段属性
- 名称：描述国际化标识
- 类型：`string`
- 默认值：`''`
- 详细：

指多语言对应的 key，不限制标识格式。

示例：

```js
{
  descriptionLangKey: 'name';
}
```

### display

- 类别：字段属性
- 名称：展示状态
- 参数：`('visible', 'hidden', 'none')`
- 类型：`string`
- 默认值：`'visible'`
- 详细：

字段展示状态分别为 显示--半隐藏(只会隐藏 UI)--全隐藏(会删除数据)。

示例：

```js
{
  display: 'visible';
}
```

### pattern

- 类别：字段属性
- 名称：UI 形态
- 类型：`string`
- 参数：`('editable', 'disabled', 'readOnly', 'readPretty')`
- 默认值：`'editable'`
- 详细：

指一个 UI 所对应的操作属性 可编辑--禁用--只读--阅读。

示例：

```js
{
  pattern: 'editable';
}
```

### valueFormatter

- 类别：字段属性
- 名称：格式化函数
- 类型：`string`
- 默认值：`''`
- 详细：

阅读模式下数据格式化函数。

示例：

```js
{
  (value) => {
    return 'string';
  };
}
```

### defaultValue

- 类别：字段属性
- 名称：默认值
- 类型：`string`
- 默认值：`''`
- 详细：

指控件初始值。

### required

- 类别：字段属性
- 名称：必填
- 类型：`Boolean`
- 默认值：`false`
- 详细：

字段是否必填，默认失去焦点时校验。

### requiredMessage

- 类别：字段属性
- 名称：必填错误消息
- 类型：`string`
- 默认值：`''`
- 详细：

必填提示消息，如果未配置此属性，将默认提示规则：\*\*不能为空。

示例：

```js
{
  requiredMessage: '**不能为空';
}
```

### requiredMessageLangKey

- 类别：字段属性
- 名称：必填消息国际化标识
- 类型：`string`
- 默认值：`''`
- 详细：

指多语言对应的 key，不限制标识格式。

示例：

```js
{
  requiredMessageLangKey: '**Cannot be empty';
}
```

### 受控中心

- 类别：字段属性
- 详细：

指配置各个组件的联动状态等。

### validator

- 类别：字段属性
- 名称：校验规则
- 类型：`undefined`
- 默认值：`undefined`
- 详细：

自定义校验规则。

### typeErrorMessage

- 类别：字段属性
- 名称：类型错误消息
- 类型：`string`
- 默认值：`''`
- 详细：

类型错误消息。

示例：

```js
{
  typeErrorMessage: '**格式校验不正确';
}
```

### typeErrorMessageLangKey

- 类别：字段属性
- 名称：类型错误消息国际化标识
- 类型：`string`
- 默认值：`''`
- 详细：

指多语言对应的 key，不限制标识格式。

示例：

```js
{
  typeErrorMessageLangKey: '**Incorrect format verification';
}
```

### 组件属性

### size

- 类别：组件属性
- 名称：尺寸
- 类型：`string|undefind`
- 参数：`('large', 'default', 'small')`
- 默认值：`undefined`
- 详细：

输入框大小。

### addonBefore

- 类别：组件属性
- 名称：前缀标签
- 类型：`string`
- 默认值：`''`
- 详细：

输入框前缀标签。

### addonAfter

- 类别：组件属性
- 名称：后缀标签
- 类型：`string`
- 默认值：`''`
- 详细：

输入框后缀标签。

### prefix

- 类别：组件属性
- 名称：前缀
- 类型：`string`
- 默认值：`''`
- 详细：

输入框前缀标签。

### suffix

- 类别：组件属性
- 名称：后缀
- 类型：`string`
- 默认值：`''`
- 详细：

输入框后缀标签。

### allowClear

- 类别：组件属性
- 名称：允许清除内容
- 类型：`boolean`
- 默认值：`false`
- 详细：

一键清除输入框内容。

### maxLength

- 类别：组件属性
- 名称：最大长度
- 类型：`number|null`
- 默认值：`null`
- 详细：

输入框显示内容最大长度。

### placeholder

- 类别：组件属性
- 名称：占位提醒
- 类型：`string`
- 默认值：`''`
- 详细：

输入框入字段提示信息,输入框无字段时显示。

### placeholderLangKey

- 类别：组件属性
- 名称：占位提示国际化标识
- 类型：`string`
- 默认值：`''`
- 详细：

占位提示多语言 key。

### onChange

- 类别：组件属性
- 名称：改值动作
- 类型：`string|undefined`
- 默认值：`undefined`
- 详细：

输入框内容发生变化时，触发事件，数据来自表单配置中的动作响应中心数据，如若已选择数据在动作响应中心被删除，此处不会自动更新选中值，请主动删除。

### onFocus

- 类别：组件属性
- 名称：获取焦点动作
- 类型：`string|undefined`
- 默认值：`undefined`
- 详细：

输入框获取焦点时，触发事件，数据来自表单配置中的动作响应中心数据，如若已选择数据在动作响应中心被删除，此处不会自动更新选中值，请主动删除。

### onBlur

- 类别：组件属性
- 名称：失去焦点动作
- 类型：`string|undefined`
- 默认值：`undefined`
- 详细：

输入失去焦点时，触发事件，数据来自表单配置中的动作响应中心数据，如若已选择数据在动作响应中心被删除，此处不会自动更新选中值，请主动删除。

### 容器属性

### tooltip

- 类别：容器属性
- 名称：提示
- 类型：`string`
- 默认值：`''`
- 详细：

输入框标题提示语。

### tooltipLangKey

- 类别：容器属性
- 名称：提示国际化标识
- 类型：`string`
- 默认值：`''`
- 详细：

输入框标题提示语国际化标识。

### labelWidth

- 类别：容器属性
- 名称：标签宽度
- 类型：`string`
- 默认值：`auto`
- 详细：

全局设置标签宽度，支持数值加单位 px、%、vh、em 或者 auto。

### wrapperWidth

- 类别：容器属性
- 名称：组件宽度
- 类型：`string`
- 默认值：`auto`
- 详细：

全局设置组件宽度，支持数值加单位 px、%、vh、em 或者 auto。

### labelCol

- 类别：容器属性
- 名称：标签栅格宽度
- 类型：`number|null`
- 默认值：`null`
- 详细：

采用 24 格栅格系统，与下面组件栅格宽度之和不能大于 24，且标签宽度和组件宽度只要其中有一个不是 auto，则栅格就不起作用。

### wrapperCol

- 类别：容器属性
- 名称：组件栅格宽度
- 类型：`number|null`
- 默认值：`null`
- 详细：

采用 24 格栅格系统，与上面标签栅格宽度之和不能大于 24，且标签宽度和组件宽度只要其中有一个不是 auto，则栅格就不起作用。

### labelAlign

- 类别：容器属性
- 名称：标签对齐方式
- 类型：`string|undefined`
- 参数：`('right', 'left')`
- 默认值：`undefined`
- 详细：

允许的对齐方式。

### wrapperAlign

- 类别：容器属性
- 名称：组件对齐方式
- 类型：`string|undefined`
- 参数：`('right', 'left')`
- 默认值：`undefined`
- 详细：

允许的对齐方式。

### hideLabel

- 类别：容器属性
- 名称：是否隐藏标签
- 类型：`boolean`
- 默认值：`false`
- 详细：

控制输入框标签显示与隐藏，表单控件可继承此属性。

### colon

- 类别：容器属性
- 名称：是否有冒号
- 类型：`boolean`
- 默认值：`true`
- 详细：

控制输入框标签冒号显示与隐藏，表单控件可继承此属性。

### asterisk

- 类别：容器属性
- 名称：是否有星号
- 类型：`boolean`
- 默认值：`true`
- 详细：

控制输入框星号显示与隐藏，表单控件可继承此属性。

### customClass

- 类别：容器属性
- 名称：自定义类名
- 类型：`Array.<string>`
- 默认值：`[]`
- 详细：

此 className 来自自定义 style 中的类名或者自己自定义。

## 多行输入

## 密码框

## 数字

## 选择框

## 复选框

## 开关

## 日期

## 日期范围

## 时间

## 时间范围

## 评分

## 级联选择

## 下拉树

## 滑动条
