<template>
  <Navigation/>
 <div id="container">
   <Overview/>
   <Features/>
 </div>
</template>

<script>
import Features from "@/components/Features";
import Overview from "@/components/Overview";
import Navigation from "@/components/Navigation";

export default {
  name: 'App',
  components: {
    Overview,
    Features,
    Navigation
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap');
/*@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;700&display=swap');*/
@font-face {
  font-family: "Material Icons Round";
  font-style: normal;
  font-weight: 400;
  src: url(https://fonts.gstatic.com/s/materialiconsround/v104/LDItaoyNOAY6Uewc665JcIzCKsKc_M9flwmP.woff2) format("woff2");
}

a{
  text-decoration: none;
}
[data-icon="true"] {
  font-family: "Material Icons Round" !important;
  font-weight: normal;
  font-style: normal;
  font-size: 24px;
  line-height: 1;
  letter-spacing: normal;
  text-transform: none;
  display: inline-block;
  white-space: nowrap;
  word-wrap: normal;
  direction: ltr;
  font-feature-settings: "liga";
  -webkit-font-smoothing: antialiased;
}


html, body {
  margin: 0;
  font-family: 'Roboto';
  --accent-color: #0095ff;
  --background-primary: #303030;
  --background-secondary: #2b2b2b;
  --background-tertiary: #282828;
  --background-quaternary: #111;
  --border-primary: #3f3f3f;
  --border-secondary: #707070;
  --color-primary: #f7f7f7;
  --color-secondary: #f5f5f5;
  --color-tertiary: #f3f3f3;
  --color-quaternary: #999;
  --boxshadow: rgb(0 0 0 / 20%) 2px 4px 10px 2px;
}

* {
  box-sizing: border-box;
}
#container{
  width: 100vw;
  height: 100vh;
  display: grid;
  grid-template-rows: repeat(2, 100%) ;
  gap: 16px;
  overflow-x: hidden;
  overflow-y: auto;
  position: relative;
  background: var(--background-tertiary);
  padding: 8px 10%;
  color: var(--color-secondary);
}

.demo-img{
  max-width: 100%;
  overflow: hidden;
  border-radius: 10px;

}
.divider{

  width: 75%;
  height: 2px;
  background: var(--border-primary);
}
.content{
  width: 100%;
  display: flex;
  align-items: center;
  gap: clamp(32px, 5%, 64px);
}
.wrapper{
  max-width: 100%;
  overflow-x: hidden;
  display: grid;
  justify-items: center;
  gap: clamp(32px, 5vh, 100px);
  align-content: center;
  height: fit-content;
}

</style>
