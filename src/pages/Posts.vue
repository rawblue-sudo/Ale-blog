<template>
  <Layout>
    <h2>Latest blog posts</h2>
    <ul>
      <li v-for="posts in $page.post" :key="edge.node.id">{{ post.title }}</li>
    </ul>
  </Layout>
</template>

<page-query>
query {
  post: post {
        id
        title 
  }
}
</page-query>
