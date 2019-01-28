# flex-direction

?> `order`属性定义项目的排列顺序。数值越小，排列越靠前，默认为 0。

```css
.item {
  order: <integer>;
}
```

<vuep template="#flex-order"></vuep>

<script v-pre type="text/x-template" id="flex-order">
<template>
  <main>
    <select v-bind:value='flexOrder.order' v-on:change="handleSelectChange">
      <option value='-6'>-6</option>
      <option value='-1'>-1</option>
      <option value='0'>0</option>
      <option value='1'>1</option>
      <option value='9'>9</option>
    </select>
    <ul>
      <li>1<br/>Order: 0</li>
      <li v-bind:style='flexOrder'>2 <br/>Order: {{flexOrder.order}}</li>
      <li>3<br/>Order: 0</li>
      <li>4<br/>Order: 0</li>
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
    flex-grow: 1;
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
      this.flexOrder.order = event.target.value
    }
  },
  data: () => ({
    flexOrder: {
      order: 0
    }
  })
}
</script>
</script>
