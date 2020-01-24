<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from "@/components/admin/AdminPostForm";

export default {
  components: {
    AdminPostForm
  },
  data() {
    return {
      loadedPost: {
        author: "Kathryn",
        title: "What do I drive?",
        content: "It all started with my dad...",
        thumbnailLink:
          "https://images.unsplash.com/photo-1577658569665-5509138cb945?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1051&q=80"
      }
    };
  }
};
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}

@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>
