# flex-basis

?> `flex-basis`属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为 auto，即项目的本来大小。

```css
.item {
  flex-basis: <length> | auto; /* default auto */
}
```

<vuep template="#flex--shrink"></vuep>

<script v-pre type="text/x-template" id="flex--shrink">
<template>
  <main>
    <select v-bind:value='flex.flexBasis' v-on:change="handleSelectChange">
      <option value='auto'>auto</option>
      <option value='80px'>80px</option>
      <option value='160px'>160px</option>
      <option value='200px'>200px</option>
    </select>
    <ul>
      <li v-bind:style='flex'>Flexbox item</li>
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
      this.flex.flexBasis = event.target.value
    }
  },
  data: () => ({
    flex: {
      flexBasis: 'auto'
    }
  })
}
</script>
</script>
