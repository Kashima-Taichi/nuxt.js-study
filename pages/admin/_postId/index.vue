<template>
  <div class="admin-post-dorm">
    <section class="update-form">
      <AdminPostsForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostsForm from "@/components/Admin/AdminPostForm";

export default {
  layout: "admin",
  components: {
    AdminPostsForm,
  },
  data() {
    return {
      loadedPost: {
        author: "Maximilian",
        title: "My awesome Post",
        content: "Super amazing, thanks for that!",
        thumbnailLink: "",
      },
    };
  },
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
