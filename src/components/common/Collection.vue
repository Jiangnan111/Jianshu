<template>
  <div>
    <br>
    <div class="container">
      <div class="row" >
        <div class="col-md-4" v-for="list in lists" :key="list.id">
          <div  class="frame">
            <router-link :to="'/c/'+list.id">
              <img style="margin-top: -50px;width: 100px;height: 100px;" :src="list.url">
              <p style="margin-top: 10px;font-size: 25px;font-weight: bold">{{list.title}}</p>
              <p>{{list.content}}</p>
            </router-link>
            <button class="button">+ 关注</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Collection",
      data(){
          return{
            lists:[
              {
                "id":1,
                "title":"读书",
                "url":"http://upload.jianshu.io/collections/images/4/sy_20091020135145113016.jpg",
                "content":"读书读书读书读书读书读书"
              },
              {
                "id":2,
                "title":"故事",
                "url":"https://upload.jianshu.io/collections/images/95/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                "content":"故事故事故事故事故事故事"
              },
              {
                "id":3,
                "title":"手绘",
                "url":"https://upload.jianshu.io/collections/images/283250/%E6%BC%AB%E7%94%BB%E4%B8%93%E9%A2%98.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                "content":"手绘手绘手绘手绘手绘手绘"
              },
              {
                "id":4,
                "title":"摄影",
                "url":"https://upload.jianshu.io/collections/images/83/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                "content":"摄影摄影摄影摄影摄影摄影"
              },
              {
                "id":5,
                "title":"@IT~互联网",
                "url":"https://upload.jianshu.io/collections/images/14/6249340_194140034135_2.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                "content":"@IT~互联网@IT~互联网@IT~互联网@IT~互联网@IT~互联网@IT~互联网"
              },
              {
                "id":6,
                "title":"自然科普",
                "url":"//upload.jianshu.io/collections/images/76/12.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
                "content":"自然科普自然科普自然科普自然科普自然科普自然科普"
              },
              {
                "id":7,
                "title":"旅行在路上",
                "url":"https://upload.jianshu.io/collections/images/13/%E5%95%8A.png?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                "content":"旅行在路上旅行在路上旅行在路上旅行在路上旅行在路上旅行在路上"
              },
              {
                "id":8,
                "title":"简书电影",
                "url":"https://upload.jianshu.io/collections/images/21/20120316041115481.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
                "content":"简书电影简书电影简书电影简书电影简书电影简书电影"
              },
              {
                "id":9,
                "title":"程序猿",
                "url":"https://upload.jianshu.io/collections/images/16/computer_guy.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
                "content":"程序猿程序猿程序猿程序猿程序猿程序猿"
              },
            ]


          }
      }
    }
</script>

<style scoped>
  .button{
    width: 100px;
    height: 40px;
    border-radius: 30px;
    border: 1px solid white;
    background-color: limegreen;
    color: white;
  }
  .frame{
    border: 1px solid lightgrey;
    border-radius: 5px;
    width: 300px;
    height: 300px;
    margin: 60px 10px 20px 20px;
    text-align: center;
    /*margin-top: 100px;*/
  }
</style>
