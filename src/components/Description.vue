<template>
  <div class="description-content">
    <div class="description column is-8 is-offset-2">
      QuickeRは，皆様のバーコードの管理を楽にします．
    </div>
    <div class="description-text column is-8 is-offset-2">
      QRコードはみなさんにとっても身近な存在だと思います．しかし，QRコードは画像であるため，管理をするのが難しいと思います．<br>
      そこで我々は，QRコードを管理して取り出したいときにすぐに取り出せる，そんなアプリを作りました．
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
})

export default class Description extends Vue {}
</script>

<style lang="scss">

.description {
  font-size: 2em;
  text-align: left;
}

.description-content {
  padding-top: 80px;
  padding-bottom: 80px;
  background-color: #192024;
  color: #FFF;
}

@media screen and (max-width: 750px) {
  .description-content {
    padding: 40px;
  }
}
</style>
