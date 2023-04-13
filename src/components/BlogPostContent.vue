<template>
    <p>{{ content }}</p>
</template>
  
<script>
export default {
    name: 'BlogPostContent',
    props: {
        content: String,
    },
    components: {
      
    }
}
</script>

<style scoped>
p {
    margin: 0;
}
</style>