<template>
  <div>
    <md-toolbar class="md-dense">
      <md-button class="md-icon-button">
        <md-icon>menu</md-icon>
      </md-button>

      <h2 class="md-title" style="flex: 1">{{title}}</h2>

    </md-toolbar>

    <router-view></router-view>
  </div>
</template>

<script lang="ts">
  import get from 'lodash.get'

  export default {
    name: 'app',
    computed: {
      title (): string {
        return get(this.$store.state, 'config.meta.title', 'Locational')
      }
    }
  }
</script>

<style>
</style>
