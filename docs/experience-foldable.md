# 展开收起效果

?> max-height

<vuep template="#experience--foldable"></vuep>

<script v-pre type="text/x-template" id="experience--foldable">
<template>
<main>
  <p>个人觉得，display:table-cell最强的应用是可以任意个数列表的等宽效果</p>
  <div v-bind:class="{foldable:true, unFold: !isFold}">
    <p>隐藏的内容...</p>
  </div>
  <span v-on:click='toggle'>{{isFold ? '更多↓' : '收起↑'}}</span>
</main>
</template>
<style>
main{
  height: 300px;
  width: 100%;
}
.foldable {
  max-height: 0;
  overflow: hidden;
  transition: max-height .25s;
}
.unFold {
  max-height: 666px;
}
</style>

<script>
module.exports = {
  methods:{
    toggle: function (event) {
    this.isFold = !this.isFold
  }
  },
  data: () => ({
    isFold: true
  })
}
</script>
</script>
