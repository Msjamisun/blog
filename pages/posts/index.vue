<template>
  <div class="post-view">
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from "@/components/posts/PostList";

export default {
  components: {
    PostList
  },
  computed: {
    loadedPosts() {
      return this.$store.getters.loadedPosts
    }
  }
};
</script>

<style scoped>
.post-view {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
