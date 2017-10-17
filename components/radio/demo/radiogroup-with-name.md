---
order: 4
title:
  zh-CN: 单选组合 - 配合 name 使用
  en-US: RadioGroup with name
---

## zh-CN

可以为 RadioGroup 配置 `name` 参数，为组合内的 input 元素赋予相同的 `name` 属性，使浏览器把 RadioGroup 下的 Radio 真正看作是一组（例如可以通过方向键始终**在同一组内**更改选项）。

## en-US

Passing the `name` property to all `input[type="radio"]` that are in the same RadioGroup. It is usually used to let the browser see your RadioGroup as a real "group" and keep the default behavior. For example, using left/right keyboard arrow to change your selection that in the same RadioGroup.

```` html
<template>
  <div>
    <radio-group v-model="checkedValue" name="radiogroup">
      <radio value="a">A</radio>
      <radio value="b">B</radio>
      <radio value="c">C</radio>
      <radio value="d">D</radio>
    </radio-group>
  </div>
</template>

<script>
  import Radio from '@/radio'
  export default {
    data () {
      return {
        checkedValue: 'a'
      }
    },
    components: {
      Radio,
      RadioGroup: Radio.Group
    }
  }
</script>
````