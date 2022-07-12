<template>
  <footer class="section wrapper footer">
    <!--    <div class="card">-->
    <!--      -->
    <!--    </div>-->
    <!--    <div class="card">-->

    <!--    </div>-->
    <!--    <div class="card">-->

    <!--    </div>-->
    <a href="https://github.com/FacoBackup" target="_blank" rel="noreferrer">
      FacoBackup
    </a>
    <div class="vert-divider"/>
    <a href="https://www.linkedin.com/in/gustavo-roque-ab85b4154/" target="_blank" rel="noreferrer">
      Gustavo Roque
    </a>
    <a style="position: absolute; right: 16px" href="https://github.com/projection-engine" target="_blank" rel="noreferrer">Projection Engine | 2022</a>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.footer {
  display: flex;
  align-items: center;
  padding: 6px 16px;
  gap: 6px;
  margin-top: 5vh;
  font-size: .8rem;

  height: 50px;
  width: 100vw;
  background: var(--background-primary);
  position: relative;
}

a {
  color: var(--color-primary);
}

a:hover {
  text-decoration: underline;
}
</style>
