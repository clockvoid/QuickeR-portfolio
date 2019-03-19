<template>
  <div class="box">
    <div>
      <p id="quicker" v-bind:class="inputClass" v-on:animationend="animationEnd">
      QuickeR
      </p>
    </div>
    <div v-bind:class="container">
      <a href='https://play.google.com/store/apps/details?id=com.qrist.quicker&pcampaignid=MKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1'><img alt='Google Play で手に入れよう' src='https://play.google.com/intl/ja/badges/images/generic/ja_badge_web_generic.png'/></a>
      <a href='https://itunes.apple.com/us/app//id1438756355?mt=8'><img id='appstore' alt='Download it on the App Store' src='../assets/appstore.svg'/></a>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop, Emit, Watch } from 'vue-property-decorator'

@Component({
  filters: {
    convertUpperCase (value: string): string | null {
      if (!value) {
        return null
      }
      return value.toUpperCase()
    }
  }
})

export default class Top extends Vue {
  @Prop()
  val!: string

  value: string = this.val
  inputValue: string = ''
  inputClassValue: string = ''
  containerValue: string = 'before'

  @Emit('handle-click') clickButton (val: string): void {}

  @Watch('value')
  onValueChange (newValue: string, oldValue: string): void {
    console.log(`watch: ${newValue}, ${oldValue}`)
  }

  @Watch('inputValue')
  onInputValueChanged (newValue: string, oldValue: string): void {
    console.log(`watch: ${newValue}, ${oldValue}`)
  }

  get isDisabled (): boolean {
    return this.inputValue === ''
  }

  get inputClass (): string {
    return this.inputClassValue
  }

  get container (): string {
    return this.containerValue
  }

  mounted (): void {
    console.log('mounted')
    this.inputClassValue = 'icon'
  }

  handleInput ($event: Event): void {
    this.inputValue = (($event.target as any) as HTMLInputElement).value
  }

  handleClick (): void {
    if (this.inputValue === '') {
      return
    }
    this.value = this.inputValue
    this.inputValue = ''
    this.clickButton(this.value)
  }

  animationEnd (): void {
    console.log('animation is ended')
    this.containerValue = 'after'
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.box {
  width: 100vw;
  height: 100vh;
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-flex-direction: column;
  -ms-flex-direction: column;
  flex-direction: column;
}

@media screen and (max-width: 320px) and (max-width: 480px) {
  .box {
    width: 320px;
    height: 480px;
  }
}

img {
  margin-top: 2.5em;
  height: 5em;
}

#appstore {
  padding: 12.4px;
}

.before {
  opacity: 0;
}

.after {
  opacity: 1;
}

.icon {
  animation-name: animateIcon;
  animation-duration: 2s;
}

@keyframes animateIcon {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

#quicker {
  font-size: 7em;
  font-weight: 400;
  font-family: 'Patua One', cursive;
}
</style>
