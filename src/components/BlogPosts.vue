<template>
    <div class="blogPosts">
        <div class="blogPosts" :key="blogPost.id" v-for="blogPost in blogPostData">
            <BlogPost :blogPost="blogPost"/>
        </div>
    </div>
</template>
  
<script>
import BlogPost from './BlogPost'

export default {
    name: 'BlogPosts',
    props: {
        blogPostData: Array,
    },
    components: {
        BlogPost,
    }
}
</script>

<style scoped>
.blogPosts {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 100%;
    gap: 1rem;
}

.blogPost {
    width: 100%;
    background-color: gray;
    border-radius: 10px;
}
</style>