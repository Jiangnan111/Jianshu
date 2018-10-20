<template>
  <div>
      <b-button-group class="mx-1"  v-for="image in imageList" >
        <img style="width: 40px; height: 40px" :img-src="image.url">
        <b-btn style="background-color:#F5F5F5;color: black;">{{image.text}}</b-btn>
      </b-button-group>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        imageList: [
          {
            "id": 1,
            "url":"//upload.jianshu.io/collections/images/4/sy_20091020135145113016.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
            "text" : "简书"
          },
          {
            "id": 2,
            "url": "https://upload.jianshu.io/admin_banners/web_images/4500/e20f8255334b480222e199011779eb8d0cdabd0e.png?imageMogr2/auto-orient/strip|imageView2/1/w/1250/h/540",
            "text" : "读书"

          },
          {
            "id": 3,
            "url": "https://upload.jianshu.io/admin_banners/web_images/4504/8f6fbad5108d79f95a0af380416da37da8263251.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/1250/h/540",
            "text" :"手绘"
          },
          {
            "id": 4,
            "url": "https://upload.jianshu.io/admin_banners/web_images/4501/572782ecf027e81f518edce85f98036e88beb290.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/1250/h/540",
            "text" : "自然科普"
          },
          {
            "id": 5,
            "url": "https://upload.jianshu.io/admin_banners/web_images/4502/25b524b6d1d21c508b7ca6a6a0a77ead48eed1b6.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/1250/h/540",
            "text":"自然-行走"
          }
        ]
      }
    }
  }
</script>

<style scoped>

</style>
