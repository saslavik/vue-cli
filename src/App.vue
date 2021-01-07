<template>
  <div class="wrapper">
    <!-- header -->
    <header>
      <div class="navbar">
        <div class="cantainer">
          <div class="navbar-content">
            <div class="logo">LOGO</div>
            <ul class="navbar-list">
              <li class="navbar-item" v-for="link in links" :key="link.title">
                <router-link
                  class="navbar-link"
                  :to="link.url"
                  :title="link.title">
                    {{ link.title }}
                </router-link>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </header>
    <router-view></router-view>
    <!-- footer -->
  </div>
</template>

<script>

export default {
  data() {
    return {
      links: [
        {
          title: 'Home',
          url: '/',
        },
        {
          title: 'Example',
          url: '/example',
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.navbar-link{
  &.router-link-exact-active {
    color: blue;
  }
}

</style>