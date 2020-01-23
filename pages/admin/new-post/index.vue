<template>
  <div class="admin-new-post-page">
    <section class="new-post-section">
        <AdminPostForm />
    </section>
  </div>
</template>

<script>
import AdminPostForm from "@/components/admin/AdminPostForm";

export default {
  components: {
    AdminPostForm
  }
};
</script>
