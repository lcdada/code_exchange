<!--  -->
<template>
  <div>
    <p>欢迎来到首页</p>
    <span class="selectPic" @click="ghPic">选照片</span>
    <div>
      <transition name="fade">
        <div v-if="show">hello world</div>
      </transition>
      <button @click="handleClick" class="btn">切换</button>
    </div>
  <div class="song">
        <p id="f" class="animated bounceOutLeft">hello</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",

  data() {
    return {
      show: true
    };
  },
  created() {
    // this.$axios.post("http://www.lkvip.com/shop/goodsList",)
    //    this.$axios.post('http://www.lkvip.com/shop/goodsList', {
    //         goods_class: 15,
    //         custom_id: 26,
    //         pageindex: 1,
    //     })
    //     .then(function (response) {
    //         console.log(response);
    //     })
    //     .catch(function (error) {
    //         console.log(error);
    //     });
  },
  components: {},
  methods: {
    ghPic() {
      this.$router.push({ path: "/detail" });
      // this.$router.push({path:'/home','query':{"card":this.cardnumber,"pasw":this.password}})
    },
    handleClick: function() {
      this.show = this.show === true ? false : true;
    },
    
  }
};
</script>
<style lang='stylus' scoped>
    .selectPic {
    display: block;
    margin: 30px auto;
    }

    .fade-enter, .fade-leave-to {
    opacity: 0;
    }

    .fade-enter-active, .fade-leave-active {
    transition: opacity 1s;
    }
    .btn
        display block
        margin 0 auto
        margin-top 50px
</style>