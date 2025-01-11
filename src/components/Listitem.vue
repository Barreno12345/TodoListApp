<script setup lang="ts">
     defineProps<{
          isChecked?: boolean;
     }>();
</script>

<template>
     <label :class="{'checked': isChecked}">
          <input 
          type="checkbox" 
          :checked="isChecked"
          @change="$emit('updateItem')"
          />
          <slot>

          </slot>
     </label>
</template>

<style scoped>

</style>