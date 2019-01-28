# flex-direction

?> `flex-direction`属性决定主轴的方向（即项目的排列方向）。

```css
.box {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

<vuep template="#flex-flex-direction"></vuep>

<script v-pre type="text/x-template" id="flex-flex-direction">
<template>
  <main>
    <select v-bind:value='flexDirection' v-on:change="handleSelectChange">
      <option value='flex-direction-row'>row</option>
      <option value='flex-direction-row-reverse'>row-reverse</option>
      <option value='flex-direction-column'>column</option>
      <option value='flex-direction-column-reverse'>column-reverse</option>
    </select>
    <ul class='flex-direction'  v-bind:id='flexDirection'>
      <li>1</li>
      <li>2</li>
      <li>3</li>
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
  }
  li{
    list-style: none;
    height: 46px;
    width: 6em;
    line-height: 1.2;
    padding: 1em;
    background: #310736;
    border-radius: 4px;
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
  .flex-direction{
    display: flex;
    flex-wrap: wrap;
  }
  #flex-direction-row{
    flex-direction: row;
  }
  #flex-direction-row-reverse{
    flex-direction: row-reverse;
  }
  #flex-direction-column{
    flex-direction: column;
  }
  #flex-direction-column-reverse{
    flex-direction: column-reverse;
  }
  #flex-direction-column>li,#flex-direction-column-reverse>li{
    width: auto;
  }
</style>
<script>
module.exports = {
  methods:{
    handleSelectChange: function (event) {
      this.flexDirection = event.target.value
    }
  },
  data: () => ({
    flexDirection: 'flex-direction-row'
  })
}
</script>
</script>
