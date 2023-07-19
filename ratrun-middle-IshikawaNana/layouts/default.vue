<template>
  <div>
    <AppHeader />
    <NuxtPage />
    <AppFooter />
  </div>
</template>

<script>
// fromの後にpathを書く。そこからインポートができる。
import { AppHeader } from "../components/organisms/AppHeader";
// import  AppHeader  from "../components/organisms/AppHeader/AppHeader.vue";
import { AppFooter } from "../components/organisms/AppFooter";
export default {
  // テンプレートで使うための宣言
  components: { AppHeader, AppFooter },
};
</script>

<style lang='scss' scoped>
</style>