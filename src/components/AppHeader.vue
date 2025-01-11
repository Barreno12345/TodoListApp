<script setup lang="ts">
</script>

<template>
     <header>
          <h1><span class="icon" aria-hidden="true"> 
               Lista de tareas </span></h1>
               <P> Metas 2025</P>
     </header>
</template>

<style scoped>

     header {
     border-bottom:rgb(255, 255, 255) solid 3px;
     background-color: #000000;

}

     header::after{
     content: '';
     display: block;
     height: 1px;
     box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.75);
          
}
h1 .icon{
     font-size: 1.5rem;
     vertical-align: middle;
}



</style>