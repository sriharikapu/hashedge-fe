<template>
  <div id="app">
    <div class="nav">
      <div class="brand">Hashedge</div>
      <ul class="nav-list">
        <li v-bind:class="{ active: $route.name === 'staking' }">
          <a href="#/staking">
            <i class="material-icons">insert_drive_file</i>
            Staking
          </a>
        </li>
        <li v-bind:class="{ active: $route.name === 'trading' }">
          <a href="#/trading">
            <i class="material-icons">group_work</i>
            Trading
          </a>
        </li>
        <li class="sep"></li>
        <li v-bind:class="{ active: $route.name === 'my_portfolio' }">
          <a href="#/my_portfolio">
            <i class="material-icons">person</i>
            My Portfolio
          </a>
        </li>
      </ul>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">
html, body {
  background-color: #455A64;
  margin: 0;
  padding: 0;
  height: 100%;
  vertical-align: middle;
}

#app {
  font-family: 'Roboto Condensed', 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  height: 100%;

  >div:last-child {
    flex: 1 1 auto;
    max-width: 805px;
    color: white;
    padding: 0 16px 16px 0;
    height: 100%;
    overflow: scroll;

    >.title {
      height: 48px;
      line-height: 48px;
      margin: 84px 0 24px 0;
      font-size: 16px;
      letter-spacing: 0.05em;

      color: #ECEFF1;
    }
  }
}

.sep {
  height: 0!important;
  border-top: 1px solid #546E7A;
}

ul {
  list-style: none;
  margin: 0;
  padding: 0;
}
</style>

<style scoped lang="scss">
.nav {
  flex: 0 1 auto;
  margin: 84px 56px;
  width: 221px;
  height: 189px;

  .brand {
    height: 48px;
    line-height: 48px;

    font-family: Eczar;
    font-size: 32px;
    letter-spacing: 0.06em;

    color: #ECEFF1;
  }

  .nav-list {
    list-style: none;
    margin: 21px 0 0 0;
    padding: 0;

    li {
      margin-bottom: 8px;
      height: 32px;
      line-height: 32px;
      font-size: 16px;

      a {
        display: flex;
        color: #90A4AE;
        text-decoration: none;

        > * {
          align-self: center;
          vertical-align: center;
        }

        .material-icons {
          padding: 8px;
          font-size: 16px;
          color: #90A4AE;
        }
      }

      &.active {
        a {
          color: #ECEFF1;
          background-color: #263238;
          border-radius: 4px;

          .material-icons {
            color: #ECEFF1;
          }
        }
      }
    }
  }
}
</style>
