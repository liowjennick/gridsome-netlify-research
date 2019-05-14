<template>
  <BlogLayout>
    <div v-html="$page.post.title"></div>
    <ul>
      <li v-html="$page.post.header"></li>
      <li v-html="$page.post.description"></li>
    </ul>
  </BlogLayout>
</template>

<page-query>
  query Post ($path: String!) {
    post: post (path: $path) {
      title
      header
      description
      content
    }
  }
</page-query>

<script>
export default {
  metaInfo () {
    return {
      title: this.$page.post.title
    }
  }
}
</script>
