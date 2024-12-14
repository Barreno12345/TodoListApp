<script setup lang="ts">

</script>

<template>
     <header>
          <h1>
               <span class="icon" aria-hidden="true">To do</span>
          </h1>
          <p> Lista de Tareas en Vue.Js 3</p>
     </header>
</template>

<style scoped>
     header {

          border-bottom: black 4px solid;
          background-color: white;

     }
     header::after{
     content: "";
     display: block;
     height: 1px;
     box-shadow: 0px 0px 10px 0px  rgba(0, 0, 0, 0.75);
}
h1{
     font-size: 2rem;
}
h1 .icon {
     font-size: 1rem;
     vertical-align: middle;
}
p {
     color: black;
     font-size: 10px;
}
p .icon{
     font-size: 1rem;
     vertical-align: middle;
     
}
</style>