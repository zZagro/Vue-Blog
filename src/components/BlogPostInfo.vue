<template>
    <p>{{ info }}</p>
</template>
  
<script>
export default {
    name: 'BlogPostInfo',
    props: {
        info: String,
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