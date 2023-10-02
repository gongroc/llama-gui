<template>
  <div class="container">

  </div>
</template>

<script setup>
import {appWindow} from "@tauri-apps/api/window"
import {onMounted, ref} from "vue";

onMounted(() => {
  appWindow.listen("tauri://blur", event => {
    appWindow.hide();
  })
})

</script>

<style lang="postcss" scoped>
.container {

}
</style>
