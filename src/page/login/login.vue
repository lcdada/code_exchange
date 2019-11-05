<template>
  <div>
    <van-cell-group>
        <van-field
            v-model="cardnumber"
            required
            clearable
            type="number"
            label="卡号"
            placeholder="请输入卡号"
        />

        <van-field
            v-model="password"
            type="password"
            label="密码"
            placeholder="请输入密码"
            required
        />
    </van-cell-group>
    <van-button type="primary" size="large" class="login" @click="goHomepage()">登录</van-button>
  </div>
</template>

<script>
    import { Field ,CellGroup,Button,Toast  } from 'vant';
    export default {
        name:'Login',
        data (){
            return {
                 cardnumber:"",
                 password:"",
            }
        },
         components:{
            [CellGroup.name]:CellGroup,
            [Field.name]:Field,
            [Button.name]:Button,
            [Toast.name]:Toast 
           
        },
        methods: {
            goHomepage(){
                console.log(this.cardnumber)
                console.log(this.password)
                if(this.cardnumber == "" || this.cardnumber == "undefined" || this.password == "" || this.password == "undefined"){
                    Toast('请正确输入卡号或密码');
                }else{
                    this.$router.push({path:'/home','query':{"card":this.cardnumber,"pasw":this.password}})
                }
            }
        },
    };
</script>

<style lang='stylus' scoped>
    .login
        margin-top 30px
</style>