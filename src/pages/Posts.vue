<template>
  <Layout>
    <h2>Latest blog posts</h2>
    <ul>
      <li v-for="edge in $page.posts.edges" :key="edge.node.id">{{ edge.node.title }}</li>
    </ul>
  </Layout>
</template>

<page-query>
query {
  posts: allPosts {
    edges {
      node {
        id
        title
      }
    }
  }
}
</page-query>
