<template>
  <Layout>
    <main>
    <h1 v-html="$page.post.title"></h1>
    <h3>By {{$page.post.author}} on {{$page.post.date}}</h3>
    <g-image :src="$page.post.thumbnail" alt="pic" style="width:10rem;"/>
    <div v-html="$page.post.content"/>
    </main>
    <Disqus shortname="portfolioblog-6" :identifier="$page.post.title"  style="width:80%;margin:0 auto;"/>

  </Layout>
</template>


<page-query>
query Post ($path:String!){
  post: post(path:$path){
    id
    title
    author
    content
    thumbnail
    date ( format : "MMMM D, YYYY")
    timeToRead
  }
}
</page-query>
