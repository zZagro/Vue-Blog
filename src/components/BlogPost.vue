<template>
    <BlogPostTitle :title="blogPost.title"/>
    <BlogPostInfo :info="blogPost.info"/>
    <BlogPostContent :content="blogPost.content"/>
</template>
  
<script>
import BlogPostTitle from './BlogPostTitle'
import BlogPostContent from './BlogPostContent'
import BlogPostInfo from './BlogPostInfo'

export default {
    name: 'BlogPost',
    props: {
        blogPost: Object
    },
    components: {
        BlogPostTitle,
        BlogPostContent,
        BlogPostInfo,
    }
}
</script>
  
<style scoped>
</style>