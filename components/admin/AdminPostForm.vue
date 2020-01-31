<template>
  <form @submit.prevent="onSave">
    <AppInputControl v-model="editedPost.author">Author Name</AppInputControl>
    <AppInputControl v-model="editedPost.title">Title</AppInputControl>
    <AppInputControl v-model="editedPost.thumbnail"
      >Thumbnail Link</AppInputControl
    >
    <AppInputControl control-type="textarea" v-model="editedPost.previewText"
      >Preview Text</AppInputControl
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
import AppInputControl from "@/components/ui/AppInputControl";
import AppButton from "@/components/ui/AppButton";

export default {
  components: {
    AppInputControl,
    AppButton
  },
  props: {
    post: {
      type: Object,
      required: false
    }
  },
  data() {
    return {
      editedPost: this.post
        ? { ...this.post }
        : {
            author: "",
            title: "",
            thumbnail: "",
            previewText: "",
            content: ""
          }
    };
  },
  methods: {
    onSave() {
      this.$emit("submit", this.editedPost);
    },
    onCancel() {
      // Navigate back
      this.$router.push("/admin");
    }
  }
};
</script>
