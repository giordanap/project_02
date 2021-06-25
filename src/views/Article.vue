<template>
  <Title :text="`Title nro ${$route.params.id}: ${article.title}`" />
  <h2>Parameter: {{$route.params.id}}</h2>
  <p>{{ article.id}} - {{ article.body}}</p>
</template>

<script>
import Title from '../components/Title.vue'
export default {
  components: {
      Title
  },
  data() {
    return {
      article: {}
    }
  },
  methods: {
    async consumeArticle() {
      try {
        const data = await fetch(`https://jsonplaceholder.typicode.com/posts/${this.$route.params.id}`)
        const object = await data.json()
        this.article = object

      } catch(error) {
        console.log(error)
      }
    }
  },
  created () {
    this.consumeArticle();
  }
}

</script>

<style>

</style> 