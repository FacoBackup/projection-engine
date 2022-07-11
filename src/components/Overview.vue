<template>
<div class="section" id="1">
   <div class="header">
     <img src="@/assets/logo.png" class="image"/>
     Projection Engine
   </div>
 </div>
</template>

<script>
export default {
  name: 'Overview'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header{
  background: var(--background-quaternary);
  color: white;
  height: 35vh;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 32px;
  font-size: 3.5rem;
  font-weight: bold;
}
.image{
  height: 9rem;
}
</style>
