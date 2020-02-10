<template>
  <div class="left-sidebar">
      <div class="search-container">
          <input type="text" placeholder="Search">
          <span class="icon"><fa :icon="['fas', 'search']" /></span>
      </div>
    sidebar =]
  </div>
</template>

<script>
export default {
}
</script>

<style lang="scss">
@import "~/assets/scss/main.scss";

    .left-sidebar {
        display: flex;
        flex: 1;
        flex-direction: column;
        height: 100%;
        width: 0;
        background: $color_dark;
        max-width: 300px;

        &.active {
            width: 300px;
        }

        .search-container {
            width: 100%;
            position: relative;
            input {
                height: 50px;
                width: 100%;
                border: none;
                background: none;
                padding: 0 10px;
                font-size: 1em;
                letter-spacing: 1px;
                outline: none;
                color: #f1f1f1;
                background: #252733;
                transition: all 0.3s;
                &:focus {
                    background: #fff;
                    color: $color_dark;
                }
            }
            .icon {
                position: absolute;
                right: 20px;
                pointer-events: none;
                cursor: none;
                z-index: 1;
                color: #f1f1f1;
                top: 0;
                font-size: 1.2em;
                line-height: 50px;
            }
        }
    }
</style>
