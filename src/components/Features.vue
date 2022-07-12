<template>
  <div class="section wrapper" style="gap: 16px; height: 100%;">
    <div class="content">
      <div style="width: 100%">
        <h1 style="text-align: left">
          Easier to work with
        </h1>
        <p><strong>Every tool on the main window</strong>: No need to have dozens of windows open to change a simple thing.</p>
        <p><strong>Flexible layout</strong>: You can create your own layout and save multiple of them to use the most suited to the situation.</p>
        <p><strong>JavaScript</strong> is one of the most used and powerful scripting languages today and it is the <strong>scripting language of choice</strong> for this engine</p>

      </div>
      <img class="demo-img" src="https://raw.githubusercontent.com/projection-engine/.github/main/development/VIEWS.png" alt="Editor"/>
    </div>
    <div class="divider"/>
    <div class="content">
      <div class="technologies">
        <div>
           React
        </div>
        <div>
          Electron
        </div>
        <div>
          Node
        </div>
        <div>
          Vue
        </div>
        <div>
          WebGL
        </div>
        <div>
          Fabric UI
        </div>
        <div>
          WebAssembly
        </div>
        <div>
          Webpack
        </div>
        <div>
          Google fonts
        </div>
        <div>
          glTF 2.0
        </div>

      </div>
      <div style="width: 100%">
        <h1 style="text-align: left">
          Fast development
        </h1>
        <p>Even though our team is small the development is very fast and new releases will come frequently</p>
        <p>
          We are using industry leading technologies to build the best editor possible and the best experience for the final user.
        </p>
      </div>
    </div>
    <div class="divider"/>
    <div class="content">
      <div style="width: 100%">
        <h1 style="text-align: left">
          Powerful features
        </h1>
        <p>
          Industry standard features are present here, including shader editing, hierarchy transformations,
          selection, hot keys, context menus for entities and more
        </p>
      </div>
      <div class="technologies">
        <div>
          Node based custom shaders
        </div>
        <div>
          Content browser
        </div>
        <div>
          Hierarchy view
        </div>
        <div>
          Entity linking
        </div>
        <div>
          Rendering channels
        </div>
        <div>
          Viewport selection
        </div>
        <div>
          Transformations gizmos
        </div>
        <div>
          3D cursor
        </div>
        <div>
          Global and local transformations
        </div>
        <div>
          Console
        </div>
        <div>
          Scripting with JavaScript
        </div>
        <div>
          Cameras
        </div>
        <div>
          Advanced lighting with probes or screen space methods
        </div>
        <div>
          Physically based rendering
        </div>
        <div>
          Forward and deferred rendering
        </div>
        <div>
          Specular reflections with probes or screen space reflections
        </div>
        <div>
          Shadows
        </div>
        <div>
          Post-processing effects
        </div>
        <div>
          Bloom
        </div>
        <div>
          FXAA
        </div>
      </div>
    </div>
   </div>
</template>

<script>
export default {
  name: 'Features'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.technologies{

  display: flex;
  flex-flow: wrap;
  gap: 8px;
  align-items: flex-start;
  justify-content: center;
  width: 100%;
}
.technologies > div {
  background: var(--border-primary);

  padding: 8px 16px;
  overflow: hidden;
  border-radius: 5px;
  font-size: .8rem;
  font-weight: 550;
  display: flex;
  gap: 4px;
}
</style>
