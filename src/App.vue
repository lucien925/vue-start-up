<template>
    <app-header></app-header>
    <app-body></app-body>
</template>

<script>
import AppHeader from './components/AppHeader';
import AppBody from './components/AppBody';

export default {
  components: {
    AppHeader, AppBody
  }
}
</script>

<style>
    * {
        margin: 0;
        padding: 0;
    }
</style>
