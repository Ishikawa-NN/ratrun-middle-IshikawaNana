<template>
  <header>
    <ul>
      <!-- <li><a href="#">ホーム</a></li>
      <li><a href="#">経営理念</a></li>
      <li><a href="#">事業理念</a></li>
      <li><a href="#">事業目的</a></li>
      <li><a href="#">お問い合わせ</a></li> -->

      <li v-for="(page, key) in pageList" :key="key">
        <!-- nuxt-linkはほぼaタグ 
        内部リンクの時のみnuxt-link-->
        <nuxt-link :to="page.to">{{ page.title }}</nuxt-link>
        <!-- :にする理由：タグの中に入れる属性のとき、変数にするため。-->
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  setup() {
    // オブジェクトの配列
    //reactiveを使う場合はオブジェクトもしくは配列のとき
    // refを使う場合は、文字列・数字・boolean型
    const pageList = reactive([
      { to: "#", title: "ホーム" },
      { to: "#", title: "私達について" },
      { to: "#", title: "選ばれる理由" },
      { to: "#", title: "ワークフロー" },
      { to: "#", title: "FAQ" },
    ]);
    return { pageList };
  },
};
</script>

<style lang='scss' scoped>
ul {
  display: flex;
  gap: 30px;
  position: absolute;
  top: 0;
  left: 0;
  li {
    list-style: none;
    a {
      text-decoration: none;
      // 後で白色にする
      color: black;
    }
  }
}
</style>