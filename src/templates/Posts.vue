<!-- src/templates/Post.vue -->
<template>
  <Layout>
    <div>
      <h1 v-html="$page.post.title" />
      <div v-html="$page.post.content" />
    </div>
  </Layout>
</template>

<page-query>
query Post ($id: ID!) {
      post(id: $id) {
        title
        content
  
  }
}
</page-query>

<script>
export default {
  metaInfo() {
    return {
      title: this.$page.post.title
    };
  }
};
</script>
