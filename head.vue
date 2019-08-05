<template>
   <header class="head">
        <a href="/index.html" class="logo">
          <img src="./image/logo.png" alt="">
        </a>
        <div>
          <ul class="head-ul">
            <li class="head-li" v-for="(item,index) in headList" :key="index">
              <a :href="item.url" class="head-a" :class="{'active' :item.flag}">{{item.val}}</a>
            </li>
          </ul>
        </div>
      </header>
</template>

<script>
export default {
  name:'head',
  data(){
    return{
      headList: [{
          val: '首页',
          url: '/index.html',
          flag: true
        },
        {
          val: '品牌入驻',
          url: './join_new.html'
        },
        {
          val: 'Fanr体验师',
          url: './agreement.html?id=2'
        },
        {
          val: '资讯中心',
          url: './news.html'
        },
        {
          val: '关于我们',
          url: './agreement.html?id=1'
        },
      ],
    }
  }
}
</script>
<style scoped>
  @import './css/global.css';
</style>

