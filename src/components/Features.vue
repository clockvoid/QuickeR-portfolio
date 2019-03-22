<template>
  <div class="feature-content">
    <div class="feature column is-8 is-offset-2">
      <div class="columns is-vcentered body">
        <div class="img-parent column is-3 is-offset-3">
          <img class="feature-img" src="../assets/home.png" />
        </div>
        <div class="column is-6">
          <div class="feature-description">
            <font-awesome-icon icon="check" />
              QRコードを一覧できます．
              <div class="description-body">
                はじめにアプリを開くとQRコードが表示されます．
              </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
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
