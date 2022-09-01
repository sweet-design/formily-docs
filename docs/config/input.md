---
title: Input component
order: 2
toc: menu
---

# Input component

It generally appears in the scenario where users need to submit information or collect user information. Currently, formily supports the following basic input components:

## Input box

Entering content through the mouse or keyboard is the most basic form field wrapper.

### Usage scenario

- When the user is required to enter the content of the form field
- Provide combined input box, with search input box and size selection

### cate

- Category: Field properties
- name: Control category
- Type: `string`
- Default value:`'input'`
- Details:

The category of the control.

### type

- Category: Field properties
- name: Control type
- Type: `string`
- Default value:`'input'`
- Details:

The type of the control.

### name

- Category: Field properties
- name: Field ID
- Type: `string`
- Default value:`''`
- Details:

Generally, it refers to the column name in the corresponding database, and only English letters can be used.

Example:

```js
{
  name: 'name';
}
```

### title

- Category: Field properties
- name: Title
- Type: `string`
- Default value:`'Input'`
- Details:

Refers to the name of the display control. If the internationalization ID is configured, the specified data will be read. Otherwise, it will be used as the default value.

Example:

```js
{
  title: 'name';
}
```

### titleLangKey

- Category: Field properties
- name: Title International logo
- Type:`string`
- Default value:`''`
- Details:

It refers to the key corresponding to multiple languages and does not limit the identification format.

Example:

```js
{
  titleLangKey: 'name';
}
```

### description

- Category: Field properties
- name: Describe
- Type:`string`
- Default value:`''`
- Details:

Simply describe or comment the field.

Example:

```js
{
  description: 'description';
}
```

### descriptionLangKey

- Category: Field properties
- name: Description International logo
- Type:`string`
- Default value:`''`
- Details:

It refers to the key corresponding to multiple languages and does not limit the identification format.

Example:

```js
{
  descriptionLangKey: 'name';
}
```

### display

- Category: Field properties
- name: Display status
- Parameters:`('visible', 'hidden', 'none')`
- Type:`string`
- Default value:`'visible'`
- Details:

The display states of the fields are displayed - half hidden (only UI will be hidden) - all hidden (data will be deleted).

Example:

```js
{
  display: 'visible';
}
```

### pattern

- Category: Field properties
- name: UI form
- Type:`string`
- Parameters:`('editable', 'disabled', 'readOnly', 'readPretty')`
- Default value:`'editable'`
- Details:

Refers to the operation attribute corresponding to a UI. It can be edited - disabled - read only - read.

Example:

```js
{
  pattern: 'editable';
}
```

### valueFormatter

- Category: Field properties
- name: Formatting Functions
- Type:`string`
- Default value:`''`
- Details:

Data formatting function in reading mode.

Example:

```js
{
  (value) => {
    return 'string';
  };
}
```

### defaultValue

- Category: Field properties
- name: Default
- Type:`string`
- Default value:`''`
- Details:

Initial value of command and control piece.

### required

- Category: Field properties
- name: Required
- Type:`Boolean`
- Default value:`false`
- Details:

Whether the field is required is checked when the focus is lost by default.

### requiredMessage

- Category: Field properties
- name: Required error message
- Type:`string`
- Default value:`''`
- Details:

Required prompt message. If this attribute is not configured, the default prompt rule will be: \* \* cannot be empty.

Example:

```js
{
  requiredMessage: '**cannot be empty';
}
```

### requiredMessageLangKey

- Category: Field properties
- name: Required message internationalization ID
- Type:`string`
- Default value:`''`
- Details:

It refers to the key corresponding to multiple languages and does not limit the identification format.

Example:

```js
{
  requiredMessageLangKey: '**Cannot be empty';
}
```

### Controlled Center

- Category: Field properties
- Details:

Refers to the linkage status of each component.

### validator

- Category: Field properties
- name: Verification rules
- Type:`undefined`
- Default value:`undefined`
- Details:

User defined verification rules.

### typeErrorMessage

- Category: Field properties
- name: Type error message
- Type:`string`
- Default value:`''`
- Details:

Type error message.

Example:

```js
{
  typeErrorMessage: '**Incorrect format verification';
}
```

### typeErrorMessageLangKey

- Category: Field properties
- name: Type error message internationalization ID
- Type:`string`
- Default value:`''`
- Details:

It refers to the key corresponding to multiple languages and does not limit the identification format.

Example:

```js
{
  typeErrorMessageLangKey: '**Incorrect format verification';
}
```

### Component properties

### size

- Category: Component properties
- name: size
- Type:`string|undefind`
- Parameters:`('large', 'default', 'small')`
- Default value:`undefined`
- Details:

Input box size.

### addonBefore

- Category: Component properties
- name: Prefix label
- Type:`string`
- Default value:`''`
- Details:

Input box prefix label.

### addonAfter

- Category: Component properties
- name: Suffix label
- Type:`string`
- Default value:`''`
- Details:

Input box suffix label.

### prefix

- Category: Component properties
- name: Prefix
- Type:`string`
- Default value:`''`
- Details:

Input box prefix label.

### suffix

- Category: Component properties
- name: Suffix
- Type:`string`
- Default value:`''`
- Details:

Input box suffix label.

### allowClear

- Category: Component properties
- name: Allow content to be cleared
- Type:`boolean`
- Default value:`false`
- Details:

One click to clear the contents of the input box.

### maxLength

- Category: Component properties
- name: Maximum length:
- Type:`number|null`
- Default value:`null`
- Details:

The input box displays the maximum length of the content.

### placeholder

- Category: Component properties
- name: Space occupying reminder
- Type:`string`
- Default value:`''`
- Details:

The prompt information of the input box is displayed when there is no field in the input box.

### placeholderLangKey

- Category: Component properties
- name: Placeholder prompt: international identification
- Type:`string`
- Default value:`''`
- Details:

Placeholder prompts multilingual keys.

### onChange

- Category: Component properties
- name: Change value action
- Type:`string|undefined`
- Default value:`undefined`
- Details:

When the content of the input box changes, an event will be triggered. The data is from the action response center data in the form configuration. If the selected data is deleted in the action response center, the selected value will not be automatically updated here. Please delete it actively.

### onFocus

- Category: Component properties
- name: Get focus action
- Type:`string|undefined`
- Default value:`undefined`
- Details:

When the input box gets the focus, an event will be triggered. The data is from the action response center data in the form configuration. If the selected data is deleted in the action response center, the selected value will not be automatically updated here. Please delete it actively.

### onBlur

- Category: Component properties
- name: Lose focus action
- Type:`string|undefined`
- Default value:`undefined`
- Details:

When the input loses focus, an event will be triggered. The data is from the action response center data in the form configuration. If the selected data is deleted in the action response center, the selected value will not be automatically updated here. Please delete it actively.

### Container properties

### tooltip

- Category: Container properties
- name: Tips
- Type:`string`
- Default value:`''`
- Details:

Input box title prompt.

### tooltipLangKey

- Category: Container properties
- name: Prompt International logo
- Type:`string`
- Default value:`''`
- Details:

The title prompt of the input box is the internationalized identifier.

### labelWidth

- Category: Container properties
- name: Label width
- Type:`string`
- Default value:`auto`
- Details:

Set the label width globally, and support value plus unit Px,%, VH, EM or auto.

### wrapperWidth

- Category: Container properties
- name: Component width
- Type:`string`
- Default value:`auto`
- Details:

Set the component width globally, and support the value plus unit Px,%, VH, EM or auto.

### labelCol

- Category: Container properties
- name: Label grid width
- Type:`number|null`
- Default value:`null`
- Details:

The 24 grid system is adopted, and the sum of the grid widths of the following components cannot be greater than 24. As long as one of the tag width and the component width is not auto, the grid will not work.

### wrapperCol

- Category: Container properties
- name: Component grid width
- Type:`number|null`
- Default value:`null`
- Details:

The 24 grid system is adopted, and the sum of the above label grid width cannot be greater than 24, and as long as one of the label width and the component width is not auto, the grid will not work.

### labelAlign

- Category: Container properties
- name: Label alignment
- Type:`string|undefined`
- Parameters:`('right', 'left')`
- Default value:`undefined`
- Details:

Allowable alignment.

### wrapperAlign

- Category: Container properties
- name: Component alignment
- Type:`string|undefined`
- Parameters:`('right', 'left')`
- Default value:`undefined`
- Details:

Allowable alignment.

### hideLabel

- Category: Container properties
- name: Hide label
- Type:`boolean`
- Default value:`false`
- Details:

Controls the display and hiding of input box labels. Form controls can inherit this property.

### colon

- Category: Container properties
- name: Is there a colon
- Type:`boolean`
- Default value:`true`
- Details:

Controls the display and hiding of input box labels and colons. Form controls can inherit this property.

### asterisk

- Category: Container properties
- name: Is there an asterisk
- Type:`boolean`
- Default value:`true`
- Details:

Controls the display and hiding of the asterisk in the input box. Form controls can inherit this property.

### customClass

- Category: Container properties
- name: Custom class name
- Type:`Array.<string>`
- Default value:`[]`
- Details:

This classname is from the class name in the custom style or customized by yourself.

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
