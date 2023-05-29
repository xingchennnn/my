<template>
  <div>
    <h1>测试v-For指令</h1>

    
    <p v-for="item in names" :key='item'>《{{item}}》</p>


    <h3>便利输出京东导航条</h3>
    <div class="tabs">
      <div v-for="k,i in tabs"  :key="k">{{i+1}}{{k}}</div>
      <!-- <div>秒杀</div> -->
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        names: ['这个杀手不太冷' , '功夫' , '功夫熊猫' , '灌篮高手'],
        tabs:['京东超市' , '秒杀' ,'京东家电','京东生鲜','拍卖','PLUS会员','便宜包邮','进口好物','电脑数码','京东五金城']
      }
    },
  }
</script>

<style lang="scss" scoped>
.tabs{
  display: flex;
  justify-content: center;
}
.tabs div{
  color:#666;
  margin: 5px;
}
</style>