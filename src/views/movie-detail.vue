<template>
  <div class="movie-detail">
    <h1 class=" red  ">电影详情</h1>
    <img :src="movie.img" alt="">
    <h3 class="lightcyan">电影名称:{{movie.name}}</h3>
    <h3>电影主演:{{movie.actors}}</h3>
    <h3>电影类型:{{movie.type}}</h3>
    <h3>上映时间:{{movie.showingon}}</h3>
    <p>简介(用双花括号):{{movie.desc}}</p>
    <p>简介(用v-text指令):<span v-text="movie.desc"></span></p>
    <p>简介(用v-text指令):<span v-html="movie.desc"></span></p>
    <hr>
    <button @click="next">换一部电影</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // 在这里声明template中需要使用的对象
      movie:{
        img: 'http://pic.imgdb.cn/item/62581b28239250f7c54743cb.jpg',
        name:'功夫',
        type:'动作',
        actors:['周星驰' , '黄圣依' , '火云邪神'],
        showingon:'2014-10-05',
        desc:'这是一部<b>史诗级电影</b>，讲述了一个可歌可泣的爱情故事'
      },
    };
  },
  methods: {
    // 换一部电影,修改movie对象的属性
    next() {
      this.movie = {
        img:'http://pic.imgdb.cn/item/639b0dbeb1fccdcd36acde2e.jpg',
        name:'灌篮高手',
        type:'动漫',
        actors:['宫城良田','樱木花道'],
        showingon:'2023-04-10',
        desc:'影片由《灌篮高手》原作者井上雄彦编剧和执导，同时是该系列第五部剧场动画，并启用全新声优阵容。以宫城良田为主线，讲述全国大赛湘北高中VS山王工业一战。'
      }
    }
  },
};
</script>

<style lang="scss" scoped>
.movie-detail img{
  width: 230px;
}
.red{
  color: red;
}
.lightcyan{
  color: lightgreen;

}

</style>