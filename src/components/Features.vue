<template>
  <div class="feature-content">
    <div class="feature column is-8 is-offset-2">
        <Feature title="QRコードを一覧できます．" body="はじめにアプリを開くとQRコードが表示されます．" :imageUrl="require('../assets/home.png')" />
        <Feature title="サービスを一覧できます．" body="設定アイコンからサービスの一覧を開くことができます．" :imageUrl="require('../assets/services.png')" />
        <Feature title="サービスを追加できます．" body="Twitter，Facebook，LINEに加えて自分で追加もできます．" :imageUrl="require('../assets/add.png')" />
        <Feature title="QRコードの登録も簡単です．" body="QRコードが含まれている画像を選択するだけで自動的にクロッピングしてくれます．" :imageUrl="require('../assets/register.png')" />
    </div>
  </div>
</template>

<script lang="ts">
import Feature from '../components/Feature.vue'
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {
    Feature
  }
})

export default class Featres extends Vue {}

</script>

<style lang="scss">
.feature-content {
  padding-top: 80px;
  padding-bottom: 80px;
}

.feature-img {
  box-shadow: 4px 0px 4px 0px rgba(0,0,0,0.12), 0px 4px 4px 0px rgba(0,0,0,0.24);
}

.feature-description {
  margin-left: 5rem;
  text-align: left;
  font-size: 2em;
}

.description-body {
  text-align: left;
  font-size: 0.5em;
}

@media screen and (max-width: 700px) {
  .feature-content {
    padding: 0xp;
  }
  .img-parent {
    margin: 40px;
  }
  .feature-description {
    margin: 40px;
  }
}
</style>
