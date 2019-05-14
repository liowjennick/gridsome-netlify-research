<template>
  <BlogLayout>
    <div v-html="$page.portfolio.title"></div>
    <ul>
      <li v-html="$page.portfolio.header"></li>
      <li v-html="$page.portfolio.objective"></li>
    </ul>
  </BlogLayout>
</template>

<page-query>
  query Portfolio ($path: String!) {
    portfolio: portfolio (path: $path) {
      title
      header
      objective
      content
    }
  }
</page-query>

<script>
export default {
  metaInfo () {
    return {
      title: this.$page.portfolio.title
    }
  }
}
</script>
