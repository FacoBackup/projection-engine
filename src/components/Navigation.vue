<template>
  <nav class="container" id="nav-wrapper">
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

    <div class="divider"/>
    <a draggable="false" href="https://github.com/projection-engine" target="_blank" rel="noreferrer">
      <button   title="Files repository">
      <span data-icon="true" style="font-size: 1.1rem">
        folder
      </span>
      </button>
    </a>
    <a draggable="false" href="https://github.com/projection-engine/editor/issues" target="_blank" rel="noreferrer" >
      <button   title="Issues and bugs">
        <span data-icon="true" style="font-size: 1.1rem">
          bug_report
        </span>
      </button>
    </a>
  </nav>
</template>

<script>
let targets = []
export default {
  name: "Navigation",
  data(){
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
      if(targets[index])
        document.getElementById("container").scrollTop = targets[index].offsetTop
    }
  },
  mounted() {
    targets = Array.from(document.querySelectorAll(`.section`))

    this.obs = new IntersectionObserver(e => {
      let intersecting = []
      e.forEach((v) => {
        if(v.isIntersecting)
          intersecting.push(v.target)
      })
      if(intersecting.length > 0)
        this.open = Math.min(...intersecting.map(i => targets.indexOf(i)).filter(i => i > -1))
    }, {rootMargin: "-50%"})

    console.log(targets)
    targets.forEach(t => {
      this.obs.observe(t)
    })
  },
  unmounted() {
    if(this.obs)
      this.obs.disconnect()
  }
}
</script>

<style scoped>
.container{

  height: fit-content;
  width: 50px;
  border-radius: 8px;
  background: var(--background-primary);
  padding: 8px;
  display: grid;
  align-items: center;
  align-content: center;
  justify-items: center;

  gap: 4px;

  position: absolute;
  top: 50%;
  left: 8px;
  transform: translate(0, -50%);
  z-index: 999;
  box-shadow: rgba(0, 0, 0, 0.2) 2px 4px 10px 2px;
}

button{
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
  border-radius: 50%;
}

button:hover{
  color: var(--accent-color);
}
button:active, button[data-highlight="true"]{
  background: var(--accent-color);
  color: white;
  font-weight: bold;
}
</style>