<template>
  <nav class="pagination">
    <router-link v-if="page > 1" :to="{ query: { page: parseInt(page) - 1} }" class="prev">&laquo; Prev</router-link>
    <router-link v-if="page < totalPage" :to="{ query: { page: parseInt(page) + 1}  }" class="next">Next &raquo;</router-link>
    <div class=center>
      <router-link :to="{name:'archive'}">Blog Archive</router-link>
    </div>
  </nav>
</template>

<script>
export default {
  props: {
    totalPage: Number,
    page: Number
  }
}
</script>
