<template>
    <div class="head" style="min-width: 1200px;">
        <div class="up">
          <div class="name">紫顺装饰</div>
          <div class="phone">
            <icon  :w="55" :h="55" name="phone2"></icon>
            15286803280
          </div>
        </div>
        <div class="down">
          <div class="downCenter">
            <div class="navigation" @click="changeBody('home')">首页</div>
            <div class="navigation" @click="changeBody('case')">案例展示</div>
            <div class="navigation" @click="changeBody('realScene')">实景展示</div>
            <div class="navigation"  @click="changeBody('Customized')"> 智能家居</div>
            <div class="navigation" @click="changeBody('homeFurnishing')">全屋定制</div>
            <div class="navigation" @click="changeBody('Village')">施工小区</div>
            <div class="navigation" @click="changeBody('setMeal')">套餐说明</div>
            <div class="navigation" @click="changeBody('contact')">联系我们</div>
          </div>

        </div>
    </div>
</template>

<script>
// import eventVue from
export default {
  name: 'upHead', // 网页顶部导航
  data () {
    return {
      props: ['changeBody']
    }
  },
  methods: {
    changeBody: function (parameter) {
      console.log(parameter)
      this.$emit('change', parameter)
    }
  }
}
</script>

<style scoped lang="less">
.head{
  color: #7e61ef;
  /*background-color: orchid;*/
  height: 130px;
  .up{
    margin: 0 auto;
    width: 1200px;
    height: 85px;
    /*background-color: antiquewhite;*/
    .name{
      float: left;
      line-height: 85px;
      font-size: 30px;
      font-weight: 600;
    }
    .phone{
      line-height: 85px;
      float: right;
      font-size: 30px;
    }
  }
  .down{
    background-color: #7e61ef;
    color: white;
    font-size: 16px;
    .downCenter{
      margin: 0 auto;
      width: 1200px;
      height: 45px;

      display: -webkit-box;
      display: -webkit-flex;
      display: -ms-flexbox;
      display: flex;

      .navigation{
        cursor:pointer;
        text-align: center;

        -webkit-box-flex: 1;
        -webkit-flex: 1;
        -ms-flex: 1;
        flex: 1;

        line-height: 45px;
      }
      .navigation:hover{
        background-color: #7e61ef - 20;
      }
    }
  }

}
</style>
