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

### type

- 类别：字段属性
- 名称：字段标识
- 类型: `string`
- 默认值：`''`
- 详细：

一般指对应数据库中的列名。

示例：

```js
{
  type: 'marginId';
}
```

### name

- 类别：字段属性
- 名称：字段标识
- 类型: `string`
- 默认值：`''`
- 详细：

指显示控件的名称，如果配置了国际化标识，将读取指定的数据，否则此处将作为默认值。

示例：

```js
{
  name: '所属组织';
}
```

### title

- 类别：字段属性
- 名称：标题国际化标识
- 类型：`string`
- 默认值：`''`
- 详细：

指多语言对应的 key，不限制标识格式。

示例：

```js
{
  title: 'marginId';
}
```

### titleLangKey

- 类别：字段属性
- 名称：描述
- 类型：`string`
- 默认值：`''`
- 详细：

指给字段进行简单描述或者备注。

示例：

```js
{
  titleLangKey: '所属组织名称';
}
```

### description

- 类别：字段属性
- 名称：描述国际化标识
- 类型：`string`
- 默认值：`''`
- 详细：

指多语言对应的 key，不限制标识格式。

示例：

```js
{
  description: 'groupName';
}
```

### descriptionLangKey

- 类别：字段属性
- 名称：展示状态
- 参数：`('visible', 'hidden', 'none')`
- 类型：`string`
- 默认值：`visible`
- 详细：

字段展示状态分别为 显示--半隐藏(只会隐藏 UI)--全隐藏(会删除数据)。

示例：

```js
{
  descriptionLangKey: 'visible';
}
```

### display

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
  display: 'editable';
}
```

### pattern

- 类别：字段属性
- 名称：格式化函数
- 类型：`string`
- 默认值：`''`
- 详细：

阅读模式下数据格式化函数。

示例：

```js
{
  (dayjs, models) => {
    return (rule, value, callback) => {
      if (callback) {
        // PC端
        if (value === 'pattern') {
          callback(new Error('开始时间不能小于结束时间'));
        } else {
          callback();
        }
      } else {
        // 移动端
        if (rule === 'pattern') {
          value.message = '开始时间不能小于结束时间';
          return false;
        } else {
          return true;
        }
      }
    };
  };
}
```

### valueFormatter

- 类别：字段属性
- 名称：默认值
- 类型：`string`
- 默认值：`''`
- 详细：

指控件初始值。

示例：

```js
{
  valueFormatter: '默认值';
}
```

### defaultValue

- 类别：字段属性
- 名称：必填
- 类型：`Boolean`
- 默认值：`false`
- 详细：

字段是否必填，默认 onBlur 时校验。

示例：

```js
{
  defaultValue: 'false';
}
```

### required

- 类别：字段属性
- 名称：必填错误消息
- 类型：`string`
- 默认值：`''`
- 详细：

必填提示消息，如果未配置此属性，将默认提示规则：${title}不能为空。

示例：

```js
{
  valueFormatter: '默认值';
}
```

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
