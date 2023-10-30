<template>
  <section class="scene-intro" id="intro">
    <div class="static-container">
      <h1 class="title">
        <span class="iuri">Ivo</span>
        <span class="func">.Portfolio()</span>
      </h1>

      <TextBlock>
        <p class="-purple">Take your time and have fun!</p>
        <p class="-gray">Fullstack Developer</p>
      </TextBlock>
    </div>
  </section>
</template>

<script>
import TextBlock from '../TextBlock.vue'

export default {
  name: 'IntroScene',
  components: { TextBlock },
}
</script>
