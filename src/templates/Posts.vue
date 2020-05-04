<!-- src/templates/Post.vue -->
<template>
  <Layout>
    <h1>{{post.title}}</h1>
    <p>{{post.content}}</p>
  </Layout>
</template>

<page-query>
query ($id: ID!) {
  post(id: $id) {
    title
    content
  }
}
</page-query>
