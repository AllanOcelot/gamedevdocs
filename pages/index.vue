<template>
    <div class="main-body-container">
      <SidebarLeft />
      <div class="main-content">
        <PostContainer />
      </div>
  </div>
</template>

<script>
import SidebarLeft from '~/components/Sidebar_left.vue'
import PostContainer from '~/components/PostContainer.vue'

export default {
  components: {
    SidebarLeft,
    PostContainer
  },
  data: function () {
    return {
      posts: 1
    }
  },
  mounted () {
    console.log('x')
    console.log(this.posts)
    const self = this
    setInterval(function () {
      console.log('xx')
      self.posts++
    }, 10000)
  }
}
</script>

<style lang="scss">
@import "~/assets/scss/main.scss";
  body {
    min-height: calc(100vh - 50px);
    line-height: 1;
    -webkit-font-smoothing: antialiased;
    background: #f1f1f1;
    font-family: 'Roboto', sans-serif;
  }

  .container {
    display: block;
    max-width: 90%;
    margin: 0 auto;
  }

  //Main body refers to the main content holder.
  .main-body-container {
    display: flex;
    flex-direction: row;
    flex: 1;
    height: calc(100vh - 100px);
  }

  .main-content {
    display: flex;
    flex: 1;
  }
</style>
