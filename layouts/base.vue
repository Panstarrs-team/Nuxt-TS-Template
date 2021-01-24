<template lang="pug">
  .layout
    nuxt
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'

@Component({})
export default class BaseLayout extends Vue {
  mounted() {
    let vh: number = window.innerHeight * 0.01
    document.documentElement.style.setProperty('--vh', `${vh}px`)
    window.addEventListener('resize', () => {
      vh = window.innerHeight * 0.01
      document.documentElement.style.setProperty('--vh', `${vh}px`)
    })
  }
}
</script>

<style lang="scss">
.layout {
  position: relative;
  display: block;
  background-color: $color-bg-primary;
  min-height: calc(var(--vh, 1vh) * 100);
}
</style>
