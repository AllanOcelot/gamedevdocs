<template>
    <header>
        <a href="/" class="main-logo">GameDevDocs</a>
        <nav class="main-nav">
          <ol>
            <li>
              <span class="icon"><fa :icon="['fa', 'envelope']" /></span>
            </li>
            <li>
              <span class="icon"><fa :icon="['fa', 'bell']" /></span>
            </li>
            <li>
              <span class="icon"><fa :icon="['fa', 'sign-in-alt']" /></span>
            </li>
          </ol>
        </nav>
    </header>
</template>

<script>
export default {
}
</script>

<style lang="scss">
@import "~/assets/scss/main.scss";

  header {
    position: sticky;
    top: 0;
    left: 0;
    width: 100%;
    height: 100px;
    background: $color_dark;
    color: #fff;

    nav {
      max-width: 500px;
      ol {
        list-style: none;
        width: auto;
        height: 100px;
        padding: 0 38px 0 0;
        li {
          display: inline-block;
          margin: 0 auto;
          line-height: 100px;
          padding: 0;
          margin: 0;
          font-size: 1.2em;
          width: 70px;
          cursor: pointer;
          text-align: center;
          transition: all 0.3s;
          &:hover,
          &.active {
            opacity: 1;
            background: $color_dark_hover;
            transition: all 0.3s;
          }
        }
      }
    }
  }

  header .main-logo {
    float: left;
    cursor: pointer;
    width: 300px;
    line-height: 100px;
    text-transform: uppercase;
    text-decoration: none;
    color: #fff;
    font-weight: 900;
    padding: 0 20px;
  }

  nav {
    float: right;
  }
</style>
