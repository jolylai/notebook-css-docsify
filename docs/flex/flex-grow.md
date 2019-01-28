# flex-grow

?> `flex-grow`属性定义项目的放大比例，默认为 0，即如果存在剩余空间，也不放大。

```css
.item {
  flex-grow: <number>; /* default 0 */
}
```

<vuep template="#flex--grow"></vuep>

<script v-pre type="text/x-template" id="flex--grow">
<template>
  <main>
    <select v-bind:value='flexGrow.flexGrow' v-on:change="handleSelectChange">
      <option value='0'>0</option>
      <option value='1'>1</option>
      <option value='2'>2</option>
      <option value='3'>3</option>
    </select>
    <ul>
      <li>1<br/>grow: 0</li>
      <li v-bind:style='flexGrow'>2 <br/>grow: {{flexGrow.flexGrow}}</li>
      <li>3<br/>grow: 0</li>
      <li>4<br/>grow: 0</li>
    </ul>
  </main>
</template>
<style>
  main{
    width: 100%;
  }
  ul{
    color: #fff;
    padding: 0;
    text-align: center;
    background: #310736;
    display: flex;
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
      this.flexGrow.flexGrow = event.target.value
    }
  },
  data: () => ({
    flexGrow: {
      flexGrow: 0
    }
  })
}
</script>
</script>

## tip

- flex-grow 定义如何按比例分配剩余空间
- 如果所有项目的 flex-grow 属性都为 1，则它们将等分剩余空间（如果有的话）。如果一个项目的 flex-grow 属性为 2，其他项目都为 1，则前者占据的剩余空间将比其他项多一倍。
