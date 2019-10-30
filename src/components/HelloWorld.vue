<template>
  <div class="hello">
    <p>{{msg }}</p>
    <div class="rem">
      <div class="item1"></div>
      <div class="item2"></div>
      <div class="item3"></div>
    </div>
  </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        data () {
            return {
                msg: 'Welcome to Your Vue.js App'
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  lang="stylus" scoped>
  .rem{
    width: 100%;
    height: 100px;
    margin: 0 auto;

    margin-top: 50px;
    display flex
    justify-content space-between
    align-items center

  }
  .item1
    width 50px
    height 50px
    background: #333;
  .item2
    width 50px
    height 50px
    background #666
  .item3
    width 50px
    height 50px
    background #999
</style>
