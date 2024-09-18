<template>
  <div>
    <header>
      <h2 v-html="$static.metadata.siteName"></h2>
      <nav>
        <g-link to="/">Home</g-link>
        <g-link to="/about">About</g-link>
        <g-link to="/blog">Blog</g-link>
      </nav>
    </header>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style scoped lang='scss'>
header {
  /* background-color: rgb(6, 6, 216); */
  background-color: $lightblue;
  color: white;
  padding: 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

nav a {
  text-decoration: none;
  padding: 1rem;
  font-size: 1.2rem;
  color: inherit;
}

h2 {
  font-size: 1.4rem;
  font-weight: 500;
}
</style>