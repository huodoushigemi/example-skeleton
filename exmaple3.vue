<script setup>
import { ref } from 'vue'

const loading = ref(false)
</script>

<template>
  <div class="box">

    <label for="loading3">点击切换</label>
    <input v-model="loading" id="loading3" type="checkbox" />
    
    <br /><br />

    <div class="col" v-skeleton.animated="loading">
      <div class="img" v-skeleton-item></div>
      <div class="price_wrap price">
        <div style="display: inline-block" v-skeleton-item>
          ¥<em>78</em><span class="decimals">.30</span>
        </div>
        <div class="dis" v-skeleton-item>6.1折</div>
        <div class="action icon-favour" v-skeleton-item>收藏</div>
        <div class="action icon-price" v-skeleton-item>降价提醒</div>
      </div>
      <div class="price_wrap">
        <span v-skeleton-item>定价</span>
        <span class="old_price" v-skeleton-item>¥129</span>
      </div>
      <div class="price_wrap title" v-skeleton-item>【正版包邮】javascript高级程序设计第4四版 js高级程序设计入门到精通 javascrip</div>
      <div class="price_wrap desc" v-skeleton-item>web前端开发经典教程JS“红宝书”全新升级，入门+实战，涵盖ECMAScript2019提供教学视频+配套编程环境可直接在线运行随书代码</div>
      <div class="book_desc">
        <span v-skeleton-item>[美]</span>
        <a v-skeleton-item>马特·弗里斯比 (Matt Frisbie) </a>
      </div>
    </div>

  </div>
</template>

<style scoped>
  .box {
    width: 390px;
    padding: 8px;
    box-sizing: content-box;
    background: #fff;
  }
  .img {
    width: 100%;
    height: 390px;
    background: url(https://tse4-mm.cn.bing.net/th/id/OIP-C.LsgCLkDltdNvjV9NSPIIkgHaJZ?pid=ImgDet&rs=1) no-repeat center/cover;
  }
  .price_wrap {
    position: relative;
    margin: 12px 18px 0 18px;
    font-size: 12px;
    line-height: 20px;
    color: #262626;
  }
  .old_price {
    text-decoration: line-through;
    margin-left: 4px;
  }
  .action {
    min-width: 4em;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 6px;
    padding: 2px 0;
    float: right;
    font-size: 9px;
    line-height: 1em;
    color: #262626;
  }
  .icon-price::before {
    content: '';
    width: 18px;
    height: 18px;
    margin-bottom: 4px;
    background: url(https://jstatic.3.cn/static/icon_price_reduce.939a24f1.png?__inline) no-repeat center/contain;
  }
  .icon-favour::before {
    content: '';
    width: 18px;
    height: 18px;
    margin-bottom: 4px;
    background: url(https://jstatic.3.cn/static/icon_favour_jd.4e212715.png?__inline) no-repeat center/contain;
  }
  .title {
    font-size: 16px;
    font-weight: 700;
    line-height: 21px;
  }
  .desc {
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    display: -webkit-box;
    height: 30px;
    max-height: 46px;
    overflow: hidden;
    text-overflow: clip;
    font-size: 12px;
    line-height: 1.3;
  }
  .price {
    font-size: 16px;
    color: #f2270c;
  }
  .price em {
    font-size: 30px;
    font-style: normal;
    line-height: 30px;
  }
  .dis {
    display: inline-block;
    margin-left: 4px;
    padding: 0 3px;
    border: 1px solid #e4393c;
    border-radius: 2px;
    font-size: 9px;
    line-height: 13px;
  }
  .book_desc {
    margin: 5px 18px 12px 18px;
    font-size: 12px;
    color: #666;
  }
  .book_desc > * {
    margin-right: 4px;
  }
  a {
    color: #4e91fe;
  }
</style>