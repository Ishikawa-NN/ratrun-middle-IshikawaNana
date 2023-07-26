<template>
  <footer>
    <div class="footer">
      <div>
        <img src="../../../assets/img/logo-2.png" alt="logo-2" />
      </div>

      <div>
        <ul>
          <li v-for="(page, key) in pageList" :key="key">
            <nuxt-link :to="page.to">{{ page.title }}</nuxt-link>
          </li>
        </ul>
      </div>

      <div>
        <ul>
          <li v-for="(page, key) in pageList2" :key="key">
            <nuxt-link :to="page.to">{{ page.title }}</nuxt-link>
          </li>
        </ul>
      </div>

      <div class="company">
        <p>
          建築・建築デザイン・原状回復・内装解体・建物解体・アスベスト除去工事はSENTIAにお任せください！
        </p>
        <p>株式会社SENTIA</p>
        <p>〒454-0982</p>
        <p>愛知県名古屋市高見1-20-2</p>
        <p>TEL:052-1212-2029</p>
      </div>
    </div>

    <div class="copyright">
      <p>Copyright(c) 店舗設計・デザイン・施工 CYPHER.AllRights Reserved</p>
    </div>
  </footer>
</template>

<script>
export default {
  setup() {
    const pageList = reactive([
      { to: "#", title: "ホーム" },
      { to: "#", title: "私達について" },
      { to: "#", title: "選ばれる理由" },
      { to: "#", title: "ワークフロー" },
      { to: "#", title: "FAQ" },
      { to: "#", title: "事例紹介" },
    ]);

    const pageList2 = reactive([
      { to: "#", title: "会社概要" },
      { to: "#", title: "お問合せ・お見積" },
      { to: "#", title: "個人情報保護法について" },
    ]);

    return { pageList, pageList2 };
  },
};
</script>

<style lang='scss' scoped>
.footer {
  display: flex;
  background-color: #66615c;
}

li {
  list-style: none;
  a {
    text-decoration: none;
    color: white;
  }
}

.company {
  color: white;
  border: 10px double white;
}
</style>