<template>
  <!-- prevent default http request -->
  <form @submit.prevent="onSave">
    <AppInputControl v-model="editedPost.title">Title</AppInputControl>
    <AppInputControl v-model="editedPost.author">Author</AppInputControl>
    <AppInputControl v-model="editedPost.thumbnailLink"
      >Thumbnail Link</AppInputControl
    >
    <AppInputControl control-type="textarea" v-model="editedPost.content"
      >Content</AppInputControl
    >
    <AppButton type="submit">Save</AppButton>
    <AppButton
      type="button"
      style="margin-left: 10px"
      btn-style="cancel"
      @click="onCanel"
      >Cancel</AppButton
    >
  </form>
</template>

<script>
import AppButton from '@/components/ui/AppButton';
import AppInputControl from '@/components/ui/AppInputControl';

export default {
  data() {
    return {
      editedPost: {
        title: "",
        author: "",
        thumbnailLink: "",
        content: ""
      }
    };
  },
  methods: {
    onSave() {
      console.log(this.editedPost);
    },
    onCancel() {
      this.$router.psuh("/admin");
    }
  },
  components: {
    AppButton,
    AppInputControl
  }
};
</script>