<template>
  <!-- .prevent default http request -->
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
      @click="onCancel"
      >Cancel</AppButton
    >
  </form>
</template>

<script>
import AppButton from "@/components/ui/AppButton";
import AppInputControl from "@/components/ui/AppInputControl";

export default {
  data() {
    return {
        // ternary operation to check if the method post has content, if not it will load the editedPost object
      editedPost: this.post
        ? { ...this.post }
        : {
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
      this.$router.push("/admin");
    }
  },
  components: {
    AppButton,
    AppInputControl
  },
  props: {
    post: {
      type: Object,
      required: false
    }
  }
};
</script>
