<template>
    <h1>{{ title }}</h1>
</template>
  
<script>
export default {
    name: 'BlogPostTitle',
    props: {
        title: String,
    },
    components: {
      
    }
}
</script>
  
<style scoped>
h1 {
    margin: 0;
}
</style>