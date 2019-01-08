# align-items

?> `align-items` 属性定义项目只有一根轴线时在交叉轴上如何对齐。

```css
.box {
  align-items: flex-start | flex-end | center | baseline | stretch;
}
```

<vuep template="#flex-align-items"></vuep>

<script v-pre type="text/x-template" id="flex-align-items">
<template>
  <main>
    <select v-bind:value='alignItems' v-on:change="handleSelectChange">
      <option value='align-items-flex-start'>flex-start</option>
      <option value='align-items-flex-end'>flex-end</option>
      <option value='align-items-center'>center</option>
      <option value='align-items-baseline'>baseline</option>
      <option value='align-items-stretch'>stretch</option>
    </select>
    <ul class='align-items' v-bind:id='alignItems'>
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
    width: calc(20% - 4px);
    background: #310736;
    border-radius: 4px;

    display: flex;
    align-items: center;
    justify-content: center;
  }
  li:nth-child(2){
    height: 96px;
  }
  li:nth-child(4){
    height: 76px;
  }
  .align-items{
    display: flex;
    flex-wrap: wrap;
  }
  #align-items-flex-start{
    align-items: flex-start;
  }
  #align-items-flex-end{
    align-items: flex-end;
  }
  #align-items-center{
    align-items: center;
  }
  #align-items-baseline{
    align-items: baseline;
  }
  #align-items-stretch{
    align-items: stretch;
  }
  #align-items-stretch>li{
    height: auto;
  }
</style>
<script>
module.exports = {
  methods:{
    handleSelectChange: function (event) {
      this.alignItems = event.target.value
    }
  },
  data: () => ({
    alignItems: 'align-items-flex-start'
  })
}
</script>
</script>

## tip

- `align-items: stretch` 时如果项目未设置高度或设为auto，将占满整个容器的高度。