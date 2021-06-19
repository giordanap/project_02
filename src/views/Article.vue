<template>
  <Title text="Path with parameters" />
  <h2>Parameter: {{ $route.params.id }}</h2>
</template>

<script>
import Title from '../components/Title.vue'
export default {
    components: {
        Title
    }
}

</script>

<style>

</style> 