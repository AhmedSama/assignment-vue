<template>
  <div class="container">
    <Article v-if="data" :data="data" />
    <div v-else>loading...</div>
  </div>
</template>

<script>
import Article from './components/Article.vue'
import {article} from './data'

export default {
  name: 'App',
  components: {
    Article
  },
  data(){
    return {
      data : null
    }
  },
  mounted(){
    this.data = article
  }
}
</script>

<style>
  .container{
    max-width: 715px;
    margin: 100px auto;
  }
</style>
