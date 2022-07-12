<template>
<div class="section wrapper" style="padding-top: 32px">
   <div class="header">
     <img src="@/assets/logo.png" class="logo"/>
     Projection Engine
   </div>

  <div class="content">
    <div style="width: 100%">
      <h1 style="text-align: left">
        Simple and open-source 3D graphics engine.
      </h1>
      <p>The <strong>Projection Engine</strong> is an open-source and free 3D engine focused on delivering high quality graphical features and easy-to-use tools.</p>
      <p>Taking inspiration from industry established engines, it will surely feel familiar to many, but simpler to work with.</p>
      <a href="https://github.com/projection-engine/editor/releases/tag/v0.2.0" target="_blank" rel="noreferrer">
        <button class="download-button">
          Download | 0.2.0 alpha
        </button>
      </a>
    </div>
    <img class="demo-img" src="https://github.com/projection-engine/.github/blob/main/development/SSR-3.png?raw=true" alt="Editor"/>
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
.download-button{
  height: 40px;
  background: white;
  color: #333;
  font-weight: 550;
  font-size: .9rem;

  border-radius: 5px;
  border: none;
  outline: none;
  cursor: pointer;
  transition: 150ms linear;
}
.download-button:hover{
  color: #0095ff;
  transform: scale(1.05);
}
.download-button:active{
  box-shadow: none;
  background: #0095ff;
  color: white;
}

.header{
  width: 100%;
  background: var(--background-quaternary);
  color: white;
  height: clamp(200px, 25vh, 300px);
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 32px;
  font-size: 3.5rem;
  font-weight: bold;
}
.logo{
  height: 9rem;
}
</style>
