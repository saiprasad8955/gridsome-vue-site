<template>
  <Layout> 
    <h1 v-html="$context.product.name"/>
    <h3>${{$context.product.price}}</h3>
    <!-- Product {{$context.product}} -->
    </Layout>
</template>