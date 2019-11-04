<template>
  <div class="hello">
    <p class="textw">{{msg }}</p>
    <div class="rem">
      <div class="item1"></div>
      <div class="item2"></div>
      <div class="item3"></div>
    </div>
     <div>
           <van-loading type="spinner" color="#ea2000" />
      </div>

  </div>
</template>

<script>
    import { Loading } from 'vant'
    export default {
        name: 'HelloWorld',
        data () {
            return {
                msg: 'Welcome to Your Vue.js App'
            }
        },
        components: {
            [Loading.name]: Loading
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style  lang="stylus" scoped>
  .textw
    font-size 20px
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
    width 10px
    height 10px
    background: #333;
  .item2
    width 10px
    height 10px
    background #666
  .item3
    width 10px
    height 10px
    background #999
</style>
