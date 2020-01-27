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
  asyncData(context, callback) {
    setTimeout(() => {
      callback(null, {
        loadedPosts: [
          {
            id: "1",
            title: "A little about why",
            previewText: "Why did I build this site?",
            thumbnail:
              "https://images.unsplash.com/photo-1552767037-d39312340e99?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80"
          },
          {
            id: "2",
            title: "My competiton history",
            previewText: "When I got bit by the comp bug...",
            thumbnail:
              "https://images.unsplash.com/photo-1532384748853-8f54a8f476e2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=400&q=60"
          },
          {
            id: "3",
            title: "2020 goals",
            previewText: "Cause its Janurary",
            thumbnail:
              "https://images.unsplash.com/photo-1519859660545-3dea8ddf683c?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=400&q=60"
          }
        ]
      });
    }, 1000);
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
