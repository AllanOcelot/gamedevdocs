<template>
  <div class="left-sidebar">
        <div class="search-container">
            <input type="text" placeholder="Search">
            <span class="icon"><font-awesome-icon :icon="['fas', 'search']" /></span>
        </div>
        <div class="link-collection">
            <a href="" class="non-icon">About</a>
            <a href="" class="non-icon">News</a>
            <ul>
                <li>
                    <a href="" target="_blank">
                        <span class="icon">
                             <font-awesome-icon :icon="['fab', 'twitter']"  />
                        </span>
                    </a>
                </li>
                <li>
                    <a href="" target="_blank">
                        <span class="icon">
                             <font-awesome-icon :icon="['fab', 'facebook']"  />
                        </span>
                    </a>
                </li>
                <li>
                    <a href="" target="_blank">
                        <span class="icon">
                             <font-awesome-icon :icon="['fab', 'youtube']"  />
                        </span>
                    </a>
                </li>
            </ul>
        </div>
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

        .link-collection {
            text-align: center;
            margin-top: auto;
            padding: 10px 10px 20px 10px;

            a {
                color: #fff;
                opacity: 0.8;
                transition: all 0.3s;
                font-size: 1.2em;
                text-decoration: none;
                &:hover {
                    opacity: 1;
                }

                &.non-icon {
                    display: inline-block;
                    font-size: 0.8em;
                    margin: 0 10px;
                    font-weight: normal;
                }
            }

            ul {
                padding: 20px 0 0 0;
                width: 100%;
                text-align: center;
                list-style: none;
                li {
                    display: inline-block;
                    margin: 0 10px;
                }
            }
        }
    }
</style>
