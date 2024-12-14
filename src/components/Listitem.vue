<script setup lang="ts">defineProps<{
     ischecked?:boolean | false 

}>()
</script>

<template>
     <label :class="{ 'checked': isChecked }"></label>
     <input type="checkbox" checked = "isChecked">
     <slot></slot>
     
</template>

<style scoped>
     label {
          cursor: pointer
     }
     .checked {
          text-decoration:line-through;
     }
</style>