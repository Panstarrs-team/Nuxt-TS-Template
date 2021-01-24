<template lang="pug">
  .top
    p Hello, World!
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'

@Component({
  layout: 'base',
})
export default class IndexPage extends Vue {}
</script>

<style lang="scss" scoped>
.top {
  @include page-base;
}
</style>
