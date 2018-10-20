<template>
  <div class="container row">
    <div class="col-md-8 row">
      <div class="col-md-8 row">
        <img :src="topic.topicUrl" class="image1">
        <div class="title">
          <a class="name">{{topic.topicName}}</a>
          <br>
          <div class="info">收录了{{topic.articleCount}}篇文章·{{topic.fans}}人关注</div>
        </div>
      </div>
      <div class="col-md-4 button">
        <button class="button1">投稿</button>
        <button class="button2">+ 关注</button>
      </div>
      <br>
      <br>
      <div>
        <b-nav tabs>
          <b-nav-item ><router-link to="tuijian"><span style="color: black">最新评论</span></router-link></b-nav-item>
          <b-nav-item><router-link to="remen"><span style="color: black">最新收录</span></router-link></b-nav-item>
          <b-nav-item><span style="color: black">热门</span></b-nav-item>
        </b-nav>
      </div>
      <br>
      <v-IndexContent></v-IndexContent>
    </div>
    <div class="col-md-4 row leftcontent">
      <div class="title " style="color: grey">专题公告<br/>欢迎关注公众号简宝玉( 公众号ID : jianshu4321 )后台回复“指南”获取玩转简书绝密珍贵资料汇总；
        有问题，找宝玉。简宝玉同志会专程为你答疑解惑关于简书的一切。<br><br/>本专题是绘画爱好者的乐园，欢迎互相分享学习;<br><br/>关于专题投稿要求详见
        <br>https://www.jianshu.com/p/153408302566<br>加入专题官方微信群，爱画画的小伙伴们都在这里！<br>进群方式:添加主编微信: lzx_122520，验证申请注明来自简书，进群后改备注打招呼发作品;
        <br><br/>专题...<p style="margin-top: 20px;font-size: 18px;color: black">分享到 weibo 微信 。。。</p>
      </div>
    </div>
  </div>
</template>

<script>
  import vIndexContent from '../common/IndexContent'

  export default {
    name: "Collection1",
    components:{
      vIndexContent
    },
    data() {
      return {
        id: this.$route.params.id,
        topic: {},
        articleList: [],
        fansList:[]
      }
    },
    activated() {
      this.id = this.$route.params.id;
      console.log(this.id);
      if (this.id == 1) {
        var t = {
          "id": 1,
          "topicName": "读书",
          "topicUrl": "http://upload.jianshu.io/collections/images/4/sy_20091020135145113016.jpg",
          "summary": "读书读书读书读书读书读书读书读书",
          "articleCount": 49535,
          "fans": 1601,
          "description":"fdfdf",
          "creator":"简书",
          "articleList":[
            {
              "id":1,
              "title":"测试文章",
              "summary":"测试文章测试文章测试文章测试文章测试文章...",
              "thumbnail":"1.png",
              "authorId":2,
              "nickname":"作者",
              "comments":1234,
              "likes":12
            }
          ],
          "fansList":[
            {
              "authorId":3,
              "avatar":"11.png"
            }
          ]
        };
        this.topic = t;
      } else {
        this.topic = {};
      }
    },
    computed: function () {
      return this.topic;
    }
  }

</script>

<style scoped>
  .leftcontent{
    margin-left: 15px;
  }
  .button{
    display: flex;
    flex-direction: row;
  }
  .title{
    margin-top: 50px;
  }
  .info{
    margin-left: 10px;
    font-size: 15px;
    color: gray;
  }
  .name{
    display: inline;
    font-size:21px;
    font-weight: 700;
    margin-top: 80%;
    margin-left: 5%;
  }
  .image1{
    margin-top: 30px;
    width: 100px;
    height: 100px;
    border-radius: 10px;
  }
  .button2{
    margin-top: 60px;
    width: 100px;
    height: 40px;
    float: right;
    border-radius: 30px;
    border: 1px solid white;
    background-color: limegreen;
    color: white;
  }
  .button1{
    margin-top: 60px;
    width: 80px;
    height: 40px;
    float: right;
    border-radius: 30px;
    border: 1px solid limegreen;
    background-color: white;
    color:limegreen;
  }
</style>



