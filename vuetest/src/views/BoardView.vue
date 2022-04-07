<template>
  <div class = "board">
    <h1>게시글 목록입니다.</h1>
    <a v-for = "p in pageNum" :key = "p">
      <router-link :to = " `/board/${p}` ">{{p}}</router-link> |
    </a>
    <router-view></router-view>
  </div>
</template>

<script>

export default {
  name: 'BoardView',
  data: () => ({
    pageNum: 3
  })
}
</script>

