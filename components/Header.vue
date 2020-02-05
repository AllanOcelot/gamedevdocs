<template>
  <div>
    <header>
      <div class="container">
        <a href="/" class="main-logo">GameDevDocs</a>
        <div class="search-container" />
        <nav class="main-nav">
          <ol>
            <li>Posts</li>
            <li>News</li>
            <li>Account</li>
          </ol>
        </nav>
      </div>
    </header>
  </div>
</template>

<script>
export default {
}
</script>

<style>
  header {
    position: sticky;
    top: 0;
    left: 0;
    width: 100%;
    height: 50px;
    background: #e6e6e6;
    color: #fff;
  }

  header .container {
    display: block;
    max-width: 1024px;
    margin: 0 auto;
  }

  header .main-logo {
    float: left;
    padding: 10px 0;
    cursor: pointer;
  }

  nav {
    float: right;
  }
</style>
