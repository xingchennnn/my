<template>
  <div>
    <h1>测试v-For指令</h1>

    
    <p v-for="item in names" :key='item'>《{{item}}》</p>


    <h3>便利输出京东导航条</h3>
    <div class="tabs">
      <div v-for="k,i in tabs"  :key="i">{{i+1}}{{k}}</div>
      <!-- <div>秒杀</div> -->
    </div>
    <hr>
    <h3>便利对象数组</h3>
    <p v-for="eid,i in movies" :key="i">
      电影id: {{eid.id}}&nbsp;&nbsp;|&nbsp;&nbsp;
      电影名称:《{{eid.name}}》&nbsp;&nbsp;|&nbsp;&nbsp;
      {{eid.duration}}分钟&nbsp;&nbsp;|&nbsp;&nbsp;
      {{eid.showingon}}上映
    </p>



  </div>
</template>

<script>
  export default {
    data() {
      return {
        names: ['这个杀手不太冷' , '功夫' , '功夫熊猫' , '灌篮高手'],
        tabs:['京东超市' , '秒杀' ,'京东家电','京东生鲜','拍卖','PLUS会员','便宜包邮','进口好物','电脑数码','京东五金城'],
        movies:[
          {id:1 , name:'杀手' , duration:114 , showingon:'05-02'},
          {id:2 , name:'功夫' , duration:124 , showingon:'01-02'},
          {id:3 , name:'熊猫' , duration:214 , showingon:'04-05'},
          {id:4 , name:'功夫熊猫' , duration:342 , showingon:'11-23'},
          {id:5 , name:'灌篮高手' , duration:93 , showingon:'07-31'},
        ],
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