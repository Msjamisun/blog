<template>
    <div class="admin-new-post-page">
        <section class="new-post-section">
            <form>
                <AppInputControl v-model="editedPost.title">Title</AppInputControl>
                <AppInputControl v-model="editedPost.author">Author</AppInputControl>
                <AppInputControl v-model="editedPost.thumbnailLink">Thumbnail Link</AppInputControl>
                <AppInputControl 
                    control-type="textarea"
                    v-model="editedPost.content">Content</AppInputControl>
                <AppButton type="submit">Save</AppButton>
                <AppButton
                    type="button"
                    style="margin-left: 10px"
                    btn-style="cancel"
                    @click="onCanel">Cancel</AppButton>
                <AppButton />
            </form>
        </section>
    </div>
</template>

<script>
import AppButton from '@/components/ui/AppButton'
import AppInputControl from '@/components/ui/AppInputControl'

export default {
    data() {
        return {
            editedPost: {
                title: '',
                author: '',
                thumbnailLink: '',
                content: ''
            }
        }
    },
    components: {
        AppButton,
        AppInputControl
    }
}
</script>