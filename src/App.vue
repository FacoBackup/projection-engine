<template>
  <div class="view">
    <Navigation/>
    <div id="container">
      <Overview/>
      <Features/>
      <Download/>
    </div>
  </div>
</template>

<script>
import Features from "@/components/Features";
import Overview from "@/components/Overview";
import Navigation from "@/components/Navigation";
import Download from "@/components/Footer";

export default {
  name: 'App',
  components: {
    Overview,
    Features,
    Navigation,
    Download
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

.view{
  display: grid;
  height: 100vh;
  width: 100vw;

  color: var(--color-secondary);
  background: var(--background-tertiary);
  overflow: hidden;
}
#container{
  width: 100%;
  height: 100%;

  display: grid;
  /*flex-direction: column; */

  gap: 25vh;
  overflow-x: hidden;
  overflow-y: auto;

  position: relative;
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
  height: fit-content;
  overflow: visible;
  display: flex;
  align-items: center;
  gap: 64px;
}
.vert-divider{
  height: 75%;
  min-width: 2px;
  background: var(--border-primary);
}
.wrapper{
  max-width: 100%;

  padding: 8px 10%;
  overflow: visible;
  display: grid;
  justify-items: center;
  gap: clamp(32px, 10vh, 92px);
  align-content: center;
}
</style>
