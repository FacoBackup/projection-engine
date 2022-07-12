<template>
  <nav class="container" id="nav-wrapper">
    <div class="header">
      <img src="@/assets/logo.png" class="logo"/>
      Projection Engine
    </div>
    <div class="vert-divider"/>
    <div class="group">
      <button :data-highlight="`${open === 0}`" data-index="0" v-on:click="onClick" title="overview">
       <span data-icon="true" style="font-size: 1.1rem">
        home
      </span>
      </button>
      <button :data-highlight="`${open === 1}`" data-index="1" v-on:click="onClick" title="More about">
      <span data-icon="true" style="font-size: 1.1rem">
        category
      </span>
      </button>
    </div>

    <div class="group" style="justify-content: flex-end">
      <a draggable="false" href="https://github.com/projection-engine" target="_blank" rel="noreferrer">
        <button title="Files repository">
        <span data-icon="true" style="font-size: 1.1rem">
          folder
        </span>
        </button>
      </a>
      <a draggable="false" href="https://github.com/projection-engine/editor/issues" target="_blank" rel="noreferrer">
        <button title="Issues and bugs">
          <span data-icon="true" style="font-size: 1.1rem">
            bug_report
          </span>
        </button>
      </a>
    </div>
  </nav>
</template>

<script>
let targets = []
export default {
  name: "Navigation",
  data() {
    return {
      open: 0,
      obs: undefined
    }
  },
  methods: {
    onClick(e) {
      const index = parseInt(e.currentTarget.getAttribute("data-index"))
      this.open = index
      console.log(index)
      if (targets[index])
        document.getElementById("container").scrollTop = targets[index].offsetTop
    }
  },
  mounted() {
    targets = Array.from(document.querySelectorAll(`.section`))

    this.obs = new IntersectionObserver(e => {
      let intersecting = []
      e.forEach((v) => {
        if (v.isIntersecting)
          intersecting.push(v.target)
      })
      if (intersecting.length > 0)
        this.open = Math.min(...intersecting.map(i => targets.indexOf(i)).filter(i => i > -1))
    }, {rootMargin: "-50%"})

    targets.forEach(t => {
      this.obs.observe(t)
    })
  },
  unmounted() {
    if (this.obs)
      this.obs.disconnect()
  }
}
</script>

<style scoped>

.header{
  width: fit-content;

  display: flex;
  align-items: center;
  gap: 4px;

  max-height: 100%;
  white-space: nowrap;

  font-size: .9rem;
  font-weight: 550;

  /*padding-right: clamp(8px, 5vw, 32px);*/

}
.logo{
  height: 50px;
}
.container {

  width: 100vw;
  height: 50px;
  background: var(--background-primary);
  padding: 4px;

  display: flex;
  align-items: center;
  gap: 10px;
  border-bottom: var(--border-primary) 1px solid;
  position: sticky;
  top: 0;

}

button {
  outline: none;
  border: none;
  background: transparent;

  color: var(--color-secondary);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0;
  height: 35px;
  width: 35px;
  cursor: pointer;
  transition: 150ms linear;
  border-radius: 5px;
}

button:hover {
  color: var(--accent-color);
}

button:active, button[data-highlight="true"] {
  background: var(--accent-color);
  color: white;
  font-weight: bold;
}
.group{
  width: 100%;
  display: flex;
  gap: 4px;
}
</style>