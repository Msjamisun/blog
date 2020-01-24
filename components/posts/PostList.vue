<template>
  <section class="post-list">
    <!-- is-admin - vue always you to use custom props in kabob case to pass to components -->
    <PostPreview
      id="1"
      :is-admin="isAdmin"
      thumbnail="https://images.unsplash.com/photo-1539798488725-7387f3229c49?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=400&q=60"
      title="A little about why"
      previewText="Why did I build this site?"
    />
    <PostPreview
      id="2"
      :is-admin="isAdmin"
      thumbnail="https://images.unsplash.com/photo-1532384748853-8f54a8f476e2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=400&q=60"
      title="My competiton history"
      previewText="When I got bit by the comp bug..."
    />
    <PostPreview
      id="3"
      :is-admin="isAdmin"
      thumbnail="https://images.unsplash.com/photo-1519859660545-3dea8ddf683c?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=400&q=60"
      title="Current 2020 Goals"
      previewText="Cause it's Janurary..."
    />
  </section>
</template>

<script>
import PostPreview from "@/components/posts/PostPreview";

export default {
  name: "PostList",
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    }
  }
};
</script>

<style scoped>
.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
