<script setup lang="ts">
     import { ref } from 'vue';
     import type { Ref } from 'vue';
     import ListItem from './ListItem.vue';
import { ElementFlags } from 'typescript';
     type Item = {
          title:string;
          checked?: boolean;
     }
     const GroupsItems: Ref<Item[]> = ref([ 
          {title: 'Leer un libro al mes', checked: true},
          {title: 'Hacer ejercicio', checked: false},
          {title: 'Aprender algo nuevo'},
     ]);

     const updateItem = (Element:Item): void => {
          const updateItem =findItemList(Element)
          if (updateItem) {
               toggleItemCheck(updateItem);
          }
     }

     const findItemList = (Element: Item): Item | undefined => {
          return GroupsItems.value.find ((elementItemInList) => elementItemInList.title === Element.title);
     }

     const toggleItemCheck = (Element:Item): void => {
          Element.checked = !Element.checked;
     }

</script>

<template>
     <ul>
          <li :key="index" v-for="(Item, index) in GroupsItems">
          <ListItem :isChecked="Item.checked" @updateItem="() => updateItem(Item)">
               {{ Item.title }}
          </ListItem>
          </li>
     </ul>

</template>

<style scoped>
     ul {
          list-style: none;

     }
     label{

          cursor: pointer;
     }
     .checked {
          text-decoration:line-through;
     }
     
</style>