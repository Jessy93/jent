<template>
  <section class="wrapper-page">
    <Header :asideData="asideData" :nav="nav" class="header" />
    <Navigation :nav="nav" />
    
    <main class="app-page">
      <router-view></router-view>
    </main>

    <StaticFooter class="footer" />
  </section>
</template>

<script>
import Header       from '@/components/Header'
import Navigation   from '@/components/Navigation'
import StaticFooter from '@/components/StaticFooter'

export default {
  name: 'default',
  components: { Header, Navigation, StaticFooter },
  data: () => ({
    asideData: { isOpen: false, },
    nav: { isOpen: false, },
  }),
}
</script>

<style lang="scss" scoped>
.app-page {
  position: relative;
  margin: 200px auto 50px;
  max-width: 1200px;
  padding: 0 30px;
  z-index: 1;
}
.wrapper-page {
  background:#0A0B11;
  width: 100vw;
  height: 100%;
}
.footer {
  position: fixed;
  bottom: 0;
  padding-bottom: 20px;
}
</style>
