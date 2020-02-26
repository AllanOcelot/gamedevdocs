<template>
    <header>
        <a href="/" class="main-logo">GameDevDocs</a>
        <nav class="main-nav">
          <ol>
            <li>
              <span class="icon"><font-awesome-icon :icon="['fa', 'envelope']" /></span>
            </li>
            <li>
              <span class="icon"><font-awesome-icon :icon="['fa', 'bell']" /></span>
            </li>
            <li>
              <span class="icon"><font-awesome-icon :icon="['fa', 'sign-in-alt']" /></span>
            </li>
          </ol>
        </nav>

        <div class="user-account-modal">
          <div class="modal-content">
            <div class="close-modal">
              <span class="icon"><font-awesome-icon :icon="['fas', 'times']" /></span>
            </div>
            <div class="account-container">
              <div class="user-login-cont">
                <div class="tabs">
                  <span>LOG IN</span>
                  <span>REGISTER</span>
                </div>
                <form action="">
                  <p>Log in to your account</p>
                  <div class="input-container">
                    <input type="text" placeholder="Username" :v-model="username">
                  </div>
                  <div class="input-container">
                    <input type="password" placeholder="Password" :v-model="pword">
                  </div>
                  <button>
                    Log in
                  </button>
                </form>
              </div>
            </div>
            <div class="promo-image">
              <p>Game Dev Docs is a community of game makers of all levels. Inspiring you to complete your project, and connect with your community easily.</p>
            </div>
          </div>
        </div>

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
    z-index: 1;

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

  .user-account-modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.6);
    z-index: 1;
    display: flex;
    height: 100%;
    align-items: center;
    justify-content: center;

    .modal-content {
      background: #fff;
      border-radius: 16px;
      width: 620px;
      display: flex;
      height: 400px;
      position: relative;

      .close-modal {
        position: absolute;
        top: -30px;
        right: -30px;
        font-size: 2em;
        color: #fff;
        opacity: 0.9;
        cursor: pointer;
        transition: opacity 0.2s;

        &:hover {
          opacity: 1;
        }
      }

      .account-container {
        display: flex;
        align-items: center;
        justify-content: center;
        min-width: 60%;
        height: 100%;
      }

      .promo-image {
        display: flex;
        height: 100%;
        flex: 1;
        background-image: url('~assets/images/modals/acc-bg.jpg');
        background-size: cover;
        background-position: center center;
        position: relative;
        pointer-events: none;
        border-radius: 0 15px 15px 0;
        overflow: hidden;
        p {
          position: absolute;
          top: 0;
          left: 0;
          display: flex;
          height: 100%;
          width: 100%;
          justify-content: center;
          align-items: center;
          padding: 0 20px;
          font-size: 20px;
          line-height: 30px;
          background: rgba(0,0,0,0.9);
        }
      }

    }

    .input-container {
      display: block;
      height: 50px;
      line-height: 50px;
      width: 100%;
      margin-bottom: 20px;
      &:last-of-type {
        margin-bottom: 40px;
      }

      input {
        width: 100%;
        border: none;
        border-bottom: 2px solid #464646;
        padding: 0 10px;
        background: none;
        font-size: 1em;
        height: 50px;
        line-height: 50px;
        transition: border-color 0.3s;
        &:focus {
          outline: none;
          border-color: #1d6bd0;
        }
      }
    }
    button {
      display: block;
      width: 100%;
      padding: 0 30px;
      color: #fff;
      font-weight: 100;
      border: none;
      background:#28384c;
      letter-spacing: 1px;
      margin: 0;
      line-height: 50px;
      height: 50px;
      opacity: 0.9;
      cursor: pointer;
      transition: all 0.3s;
      &:hover {
        opacity: 1;
      }
    }
  }

</style>
