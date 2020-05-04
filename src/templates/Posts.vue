<!-- src/templates/Post.vue -->
<template>
  <Layout>
    <div v-for="edge in $page.posts.edges" :key="edge.node.id">
      <h2>{{ edge.node.title }}</h2>
    </div>
  </Layout>
</template>

<page-query>
query ($id: ID!) {
  edges {
    node {
      post(id: $id) {
        title
        content
      }
    }
  }
}
</page-query>
