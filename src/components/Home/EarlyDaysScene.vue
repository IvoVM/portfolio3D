<template>
  <div class="earlyDays">
    <TitleSection scene="earlyTitle">
      <TitleFunction
        params="2019,2021"
        subtitle="&lt;MybeginningAsADeveloper&gt;&lt;tr&gt;&lt;td&gt;..."
        >earlyDays</TitleFunction
      >

      <div class="clouds cloud-1"></div>
      <Pepe v-bind="{ isPlaying }" />
      <div class="clouds cloud-2"></div>
      <div class="clouds cloud-3"></div>
      <Ocean v-bind="{ isPlaying }" />
    </TitleSection>

    <SceneSection id="early-days">
      <TextBlock>
        <p>Enthusiasm and imagination.</p>
        <p class="-big">
          A Javascript developer<br />
          <span class="-purple">with a mission in mind.</span>
        </p>
      </TextBlock>
    </SceneSection>
    <SceneSection id="early-days2">
      <TextBlock>
        <p class="-big">
          <span class="-purple">Freelancing</span> &
          <span class="-purple">startuping,</span><br />
        </p>
        <p>
          I began my adventure in web development, programming games in Unity,
          then web pages in jquery and mysql, and then perfected myself in
          fullstack development in javascript, carrying out several projects
          along the way for SMEs in my city.<br />
        </p>
      </TextBlock>
    </SceneSection>
    <SceneSection id="early-days3">
      <TextBlock>
        <p>
          Among my first projects are<br />
          <span class="-big -purple"
            ><em>El semanario</em>, <em>Fmmastermiramar</em>, Medicina Miramar,
            <em>Las Gaviotas Restaurant</em></span
          >
          and many others...
        </p>
      </TextBlock>
    </SceneSection>
  </div>
</template>

<script>
import Pepe from '../Characters/Pepe/Pepe.vue'
import Ocean from '../Characters/Ocean/Ocean.vue'
import TitleSection from '../TitleSection.vue'
import TitleFunction from '../TitleFunction.vue'
import TextBlock from '../TextBlock.vue'
import SceneSection from '../SceneSection.vue'

export default {
  name: 'EarlyDaysScene',
  components: {
    TitleSection,
    Pepe,
    Ocean,
    TitleFunction,
    TextBlock,
    SceneSection,
  },
  props: {
    isPlaying: Boolean,
  },
}
</script>

<style lang="scss">
.earlyDays {
  .pepe {
    position: absolute;
    z-index: 2;
    top: 50%;
    left: 100%;
    transform: scale(0.4) translate3d(0, -50%, 0);
    transform-origin: 0 0;
    display: none;

    @media screen and (max-width: 568px) {
      transform: scale(0.2) translate3d(0, -50%, 0);
    }
  }

  .clouds {
    position: absolute;
    width: 150vw;
    height: 150vh;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transform-origin: 50% 50%;
    background: url('../Characters/Pepe/assets/clouds-1.png') no-repeat center;
    background-size: contain;
    opacity: 0.5;

    &.cloud-2 {
      background-image: url('../Characters/Pepe/assets/clouds-2.png');
    }

    &.cloud-3 {
      background-image: url('../Characters/Pepe/assets/clouds-3.png');
      width: 100vw;
      height: 100vh;
      z-index: -1;
      opacity: 0.25;
    }
  }
}
</style>
