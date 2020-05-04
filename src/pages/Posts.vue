<template>
  <Layout>
    <h2>Latest blog posts</h2>
    <ul>
      <li v-for="posts in $page.post" :key="post.id">{{ post.title }}</li>
    </ul>
  </Layout>
</template>

<page-query>
query {
  post: post(id: $id) {
        id
        title 
  }
}
</page-query>
