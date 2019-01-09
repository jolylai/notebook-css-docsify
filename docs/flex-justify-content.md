# justify-content

?> `justify-content`属性定义了项目在主轴上的对齐方式。

```css
.box {
  justify-content: flex-start | flex-end | center | space-between | space-around;
}
```

<vuep template="#flex-justify-content"></vuep>

<script v-pre type="text/x-template" id="flex-justify-content">
<template>
  <main>
    <select v-bind:value='justifyContent' v-on:change="handleSelectChange">
      <option value='justify-content-flex-start'>flex-start</option>
      <option value='justify-content-flex-end'>flex-end</option>
      <option value='justify-content-center'>center</option>
      <option value='justify-content-space-between'>space-between</option>
      <option value='justify-content-space-around'>space-around</option>
    </select>
    <ul class='justify-content'  v-bind:id='justifyContent'>
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
  .justify-content{
    display: flex;
    flex-wrap: wrap;
  }
  #justify-content-flex-start{
    justify-content: flex-start;
  }
  #justify-content-flex-end{
    justify-content: flex-end;
  }
  #justify-content-center{
    justify-content: center;
  }
  #justify-content-space-between{
    justify-content: space-between;
  }
  #justify-content-space-around{
    justify-content: space-around;
  }
</style>
<script>
module.exports = {
  methods:{
    handleSelectChange: function (event) {
      this.justifyContent = event.target.value
    }
  },
  data: () => ({
    justifyContent: 'justify-content-flex-start'
  })
}
</script>
</script>
