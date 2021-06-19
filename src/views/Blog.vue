<template>
  <Title text="Title of my Blog"/>
  <button @click="consumeApi" >Consume an API</button>
  <div v-for="item in arrayBlog" :key="item.id">
    {{ item.id }} - {{ item.title }}
  </div>
</template>

<script>
import Title from '../components/Title.vue'
export default {
  components: {
    Title
  },
  data() {
    return {
      arrayBlog: []
    }
  },
  methods: {
    async consumeApi() {
      try {
        const data = await fetch('https://jsonplaceholder.typicode.com/posts')
        const array = await data.json()
        this.arrayBlog = array
        console.log(array)
        
      } catch(error) {
        console.log(error)
      }
  }
  }
}
</script>
