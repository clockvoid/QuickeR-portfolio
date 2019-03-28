<template>
  <div class="quicker-footer">
    Copyright <font-awesome-icon :icon="['far', 'copyright']" />
      2019 QuickeR production team, All Rights Reserved.
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
})

export default class Footer extends Vue {}

</script>

<style lang="scss">
.quicker-footer {
  padding-top: 1.4em;
  padding-bottom: 1.4em;
  background-color: #192024;
  color: #FFF;
}
</style>
