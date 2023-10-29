<script setup lang="ts">
  import DaisyUIModal from "./components/DaisyUIModal.vue";
</script>

<template>
  <DaisyUIModal>
    <!-- <template #title>Modal title</template> -->
    <template #default>Default slot</template>
    <template #text="{short}">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est sapiente</p>
      <p v-if="!short">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est sapiente</p>
    </template>
  </DaisyUIModal>
  
</template>
