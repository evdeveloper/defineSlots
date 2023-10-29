<script setup lang="ts">
  const slots = defineSlots<{
    title?: (props: { msg?: string }) => any
    text?: (props: { short: boolean }) => any
    default?:(prors: {}) => any
  }>()
</script>


<template>
  <dialog id="my_modal_1" class="modal" open>
  <div class="modal-box">
    <h3 class="font-bold text-lg">
      <slot name="title" />
      <p v-if="!slots.title">Some text</p>
    </h3>
    <slot name="text" :short="true" />
    <slot></slot>
    <div class="modal-action">
      <form method="dialog">
        <button class="btn">Close</button>
      </form>
    </div>
  </div>
</dialog>
</template>