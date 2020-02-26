<template>
  <div class="post-container">
    <transition-group name="slide-fade" appear>
      <div class="block" v-for="post in posts" :key="post">
        <div class="image-container" style="background-image: url('https://loremflickr.com/300/300')"></div>
        <div class="content-container">
          <div class="header">
            <p class="title">
              This is an example game blog title
            </p>
          </div>
          <div class="content">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat odit ipsam officiis id,
              minima similique architecto incidunt corporis nemo molestias dolorum atque sunt laboriosam?
              Porro dolor iste vitae non officiis.
            </p>
          </div>
          <div class="actions">
            buttons will go here
          </div>
        </div>
    </div>
  </transition-group>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="scss">
@import "~/assets/scss/main.scss";

.post-container {
  display: flex;
  height: 100%;
  overflow-x: hidden;
  overflow-y: auto;
  padding: 40px 20px;
  flex-direction: column;

   .block {
    display: flex;
    flex-direction: column;
    width: calc(100% - 100px );
    margin: 0 0 40px 0;
    position: relative;
    min-height: 200px;
    padding: 20px;
    box-sizing: border-box;
    margin-left: 100px;
    border-radius: 16px;
    padding-left: 120px;
    background: #fff;
    display: block;
    height: 300px;
    width: 100%;
    border: 1px solid gray;
    margin: 0 0 20px 0;

    .content-container {
      display: flex;
      flex-direction: column;
      flex: 1;

      .header {
        width: 100%;
        height: 50px;
        p.title {
          font-size: 1.4em;
          letter-spacing: 1px;
          font-weight: 900;
          line-height: 50px;
          margin:0;
          line-height: normal;
          font-weight: 600;
          cursor: default;
        }
      }
      .content {
        flex: 1;
        height: 100px;
        width: 100%;
        margin: 0;
        p {
          font-size: 1em;
          line-height: 1.5em;
          cursor: default;
        }
      }
      .actions {
        align-self: flex-end;
      }
    }
    .image-container {
      display: inline-block;
      width: 200px;
      display: flex;
      border-radius: 50%;
      overflow: hidden;
      height: 200px;
      position: absolute;
      left: -88px;
      top: 0;
      border: 10px solid #fff;
      background-color: #fff;
      background-size: cover;
      background-position: center center;
    }
  }
}
</style>
