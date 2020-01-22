<template>
<div class="post-view">
     <PostList />
</div>
</template>

<script>
import PostList from '@/components/posts/PostList'
export default {
    components: {
        PostList
    }
}
</script>

<style scoped>
.post-view {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>