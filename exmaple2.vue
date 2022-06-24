<script setup>
import { ref } from 'vue'

const loading = ref(false)
</script>

<template>
  <div>

    <label for="loading2">点击切换</label>
    <input v-model="loading" id="loading2" type="checkbox" />
    
    <br /><br />

    <div class="card" v-skeleton="loading">
      <div class="avatar" v-skeleton-item />
      <div class="header">
        <span class="title" v-skeleton-item>姬坂乃爱</span>
        <div class="time" v-skeleton-item>04-29</div>
        <div class="more" v-skeleton-item></div>
      </div>
      <div class="text" v-skeleton-item>最最可爱的我穿最最可爱的衣服就无敌了</div>
      <div class="footer">
        <div class="action icon-forward" v-skeleton-item>转发</div>
        <div class="action icon-comment" v-skeleton-item>评论</div>
        <div class="action icon-like" v-skeleton-item>点赞</div>
      </div>
    </div>

  </div>
</template>

<style scoped>
  .card {
    position: relative;
    max-width: 420px;
    padding-left: 88px;
    padding-right: 12px;
    border-radius: 4px;
    background: #fff;
    overflow: hidden;
  }
  .avatar {
    position: absolute;
    top: 24px;
    left: 24px;
    width: 48px;
    height: 48px;
    /* margin: 24px; */
    border-radius: 48px;
    background: url(https://img2.baidu.com/it/u=2181406519,969535439&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500) no-repeat center/cover;
  }
  .header {
    position: relative;
    padding-top: 27px;
  }
  .title {
    font-size: 16px;
    cursor: pointer;
    color: rgb(251, 114, 153);
  }
  .time {
    margin: 4px 0;
    width: fit-content;
    height: 14px;
    font-size: 12px;
    line-height: 18px;
    user-select: none;
    color: #99a2aa;
    cursor: pointer;
  }
  .more {
    position: absolute;
    right: 16px;
    top: 30px;
    width: 16px;
    height: 16px;
    cursor: pointer;
    background-image: url(data:image/svg+xml;base64,PHN2ZyBkYXRhLW5hbWU9IuWbvuWxgiAxIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA0MCA0MCI+PHBhdGggZD0iTTIwIDguODlhNC40NCA0LjQ0IDAgMTE0LjQ0LTQuNDRBNC40NCA0LjQ0IDAgMDEyMCA4Ljg5em0wIDE1LjU2QTQuNDQgNC40NCAwIDExMjQuNDQgMjAgNC40NCA0LjQ0IDAgMDEyMCAyNC40NHpNMjAgNDBhNC40NCA0LjQ0IDAgMTE0LjQ0LTQuNDRBNC40NCA0LjQ0IDAgMDEyMCA0MHoiIGZpbGw9IiNjY2QwZDciLz48L3N2Zz4=);
  }
  .text {
    margin-top: 10px;
    font-size: 14px;
    line-height: 22px;
    color: #222;
  }
  .footer {
    margin: 14px 0;
    display: flex;
    height: 22px;
    box-sizing: border-box;
  }
  .action {
    display: flex;
    align-items: center;
    width: 88px;
    margin-right: 4px;
    font-size: 12px;
    color: #99a2aa;
    cursor: pointer;
    user-select: none;
  }
  .action:hover {
    color: #00a1d6;
  }
  .icon-forward::before {
    content: '';
    height: 16px;
    margin-right: 4px;
    width: 20px;
    background: url(data:image/svg+xml;base64,PHN2ZyBkYXRhLW5hbWU9IuWbvuWxgiAxIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA0MCA0MCI+PHBhdGggZD0iTTMxLjM1IDM2LjE1SDguMjVBNy4xNyA3LjE3IDAgMDExIDI5LjA4di0xOC41QTcuMTggNy4xOCAwIDAxOC4yNSAzLjVoMTN2M2gtMTNBNC4xNyA0LjE3IDAgMDA0IDEwLjU4djE4LjVhNC4xNyA0LjE3IDAgMDA0LjI1IDQuMDhoMjMuMWE0LjE3IDQuMTcgMCAwMDQuMjUtNC4wN1YyMC4yaDN2OC45YTcuMTcgNy4xNyAwIDAxLTcuMjUgNy4wNXoiIGZpbGw9IiM5OWEyYWEiLz48cGF0aCBkPSJNMTUgMjMuNjRsLTIuNzgtMS4xMy41Ni0xLjM5QzE0LjgyIDE2LjA3IDIwLjU3IDExIDI3LjU5IDExaDRsLTYuMTItNiAyLjA5LTIuMTVMMzguOTUgMTRIMjcuNTljLTUuNjMgMC0xMC40IDQuMjctMTIgOC4zeiIgZmlsbD0iIzk5YTJhYSIvPjwvc3ZnPg==) no-repeat center/contain;
  }
  .icon-comment::before {
    content: '';
    height: 16px;
    margin-right: 4px;
    width: 20px;
    background: url(data:image/svg+xml;base64,PHN2ZyBkYXRhLW5hbWU9IuWbvuWxgiAxIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA0MCA0MCI+PHBhdGggZD0iTTE0LjQ2IDMuMzNoMTEuMTJjNy42NCAwIDEzLjkgNiAxMy45IDEzLjMzUzMzLjIyIDMwIDI1LjU4IDMwaC0uNzZsLTcuMjggNi42Ny0yLTYuNjdoLTEuMDhDNi44MSAzMCAuNTYgMjQgLjU2IDE2LjY3UzYuODEgMy4zMyAxNC40NiAzLjMzek0zNi43IDE2LjY3QTEwLjkxIDEwLjkxIDAgMDAyNS41OCA2SDE0LjQ2QTEwLjkxIDEwLjkxIDAgMDAzLjM0IDE2LjY3YTEwLjkxIDEwLjkxIDAgMDAxMS4xMiAxMC42NmgzLjE5bC41OCAxLjkzLjcyIDIuNDIgNC0zLjYyLjgxLS43NGgxLjg4QTEwLjkxIDEwLjkxIDAgMDAzNi43IDE2LjY3eiIgZmlsbD0ic2lsdmVyIi8+PC9zdmc+) no-repeat center/contain;
  }
  .icon-like {
    color: rgb(0, 161, 214);
  }
  .icon-like::before {
    content: '';
    height: 16px;
    margin-right: 4px;
    width: 20px;
    background: url(data:image/svg+xml;base64,PHN2ZyBkYXRhLW5hbWU9IuWbvuWxgiAxIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAzOC44OSAzNC40NyI+PHBhdGggZD0iTTExLjUgMzQuNDVWOS42MWgtLjE1bDYuNy04LjM3YTMuODMgMy44MyAwIDAxNi42NCAyLjk0bC0uMjUgNS41NWgxMC40MmE0LjE1IDQuMTUgMCAwMTMuMzMgMS42NyA0LjM4IDQuMzggMCAwMS41NiAzLjQ3TDM0LjMgMjkuNTlhNi4zNyA2LjM3IDAgMDEtNiA0Ljg2em0tMi41IDBINWE0LjUyIDQuNTIgMCAwMS00LjMxLTIuMzYgNS42MSA1LjYxIDAgMDEtLjY5LTIuNVYxNC43M2E0LjkzIDQuOTMgMCAwMTIuNS00LjMxQTguMzggOC4zOCAwIDAxNSA5LjczaDR6IiBmaWxsPSIjMDBhMWQ2Ii8+PC9zdmc+) no-repeat center/contain;
    background-size: 15px;
  }
</style>