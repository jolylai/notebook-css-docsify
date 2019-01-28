# align-content

?> align-content 属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。

```css
.box {
  align-content: flex-start | flex-end | center | space-between | space-around | stretch;
}
```

<vuep template="#flex-align-content"></vuep>

<script v-pre type="text/x-template" id="flex-align-content">
<template>
  <main>
    <select v-bind:value='alignContent' v-on:change="handleSelectChange">
      <option value='align-content-flex-start'>flex-start</option>
      <option value='align-content-flex-end'>flex-end</option>
      <option value='align-content-center'>center</option>
      <option value='align-content-space-between'>space-between</option>
      <option value='align-content-space-around'>space-around</option>
      <option value='align-content-stretch'>stretch</option>
    </select>
    <ul class='align-items'  v-bind:id='alignContent'>
      <li>1</li>
      <li>2</li>
      <li>3</li>
      <li>4</li>
      <li>5</li>
    </ul>
  </main>
</template>
<style>
  main{
    width: 100%;
  }
  ul{
    height: 300px;
    color: #fff;
    text-align: center;
  }
  li{
    list-style: none;
    height: 46px;
    margin: 2px;
    width: 30%;
    background: #310736;
    border-radius: 4px;

    display: flex;
    align-items: center;
    justify-content: center;
  }
  li:nth-child(2){
    height: 96px;
  }
  .align-items{
    display: flex;
    flex-wrap: wrap;
  }
  #align-content-flex-start{
    align-content: flex-start;
  }
  #align-content-flex-end{
    align-content: flex-end;
  }
  #align-content-center{
    align-content: center;
  }
  #align-content-space-between{
    align-content: space-between;
  }
  #align-content-space-around{
    align-content: space-around;
  }
  #align-content-stretch{
    align-content: stretch;
  }
</style>
<script>
module.exports = {
  methods:{
    handleSelectChange: function (event) {
      this.alignContent = event.target.value
    }
  },
  data: () => ({
    alignContent: 'align-content-stretch'
  })
}
</script>
</script>
