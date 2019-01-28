# flex-shrink

?> `flex-shrink`属性定义了项目的缩小比例，默认为 1，即如果空间不足，该项目将缩小。

```css
.item {
  flex-shrink: <number>; /* default 1 */
}
```

<vuep template="#flex--shrink"></vuep>

<script v-pre type="text/x-template" id="flex--shrink">
<template>
  <main>
    <select v-bind:value='flex.flexShrink' v-on:change="handleSelectChange">
      <option value='0'>0</option>
      <option value='1'>1</option>
      <option value='2'>2</option>
      <option value='3'>3</option>
    </select>
    <ul>
      <li v-bind:style='flex'>This is the flex-shrink target</li>
      <li>Foo ba</li>
      <li>3<br/>Lorem ipsum</li>
    </ul>
  </main>
</template>
<style>
  main{
    width: 100%;
  }
  ul{
    color: #fff;
    padding: 10px;
    text-align: center;
    background: #310736;
    display: flex;
    width: 300px;
  }
  li{
    list-style: none;
    padding: 1em;
  }
  li:nth-child(1){
    background: #05ffb0;
  }
  li:nth-child(2){
    background: #00d1b2;
  }
  li:nth-child(3){
    background: #ff3860;
  }
  li:nth-child(4){
    background: #ffdd57;
  }
</style>
<script>
module.exports = {
  methods:{
    handleSelectChange: function (event) {
      this.flex.flexShrink = event.target.value
    }
  },
  data: () => ({
    flex: {
      flexShrink: 1
    }
  })
}
</script>
</script>

## tip

- flex-grow 定义如何按比例分配剩余空间
- 如果所有项目的 flex-grow 属性都为 1，则它们将等分剩余空间（如果有的话）。如果一个项目的 flex-grow 属性为 2，其他项目都为 1，则前者占据的剩余空间将比其他项多一倍。
