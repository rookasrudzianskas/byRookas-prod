<template>
  <div class="earlyDays">
    <TitleSection scene="earlyTitle">
      <TitleFunction
        params="2011,2018"
        subtitle="&lt;table&gt;&lt;tr&gt;&lt;td&gt;..."
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
        <p>Design & illustration.</p>
        <p class="-big">
          A frontend developer<br />
          <span class="-purple">with one foothold in startups space.</span>
        </p>
      </TextBlock>
    </SceneSection>
    <SceneSection id="early-days2">
      <TextBlock>
        <p class="-big">
          <span class="-purple">Freelancing</span> &
          <span class="-purple">startuping,</span><br />
          <span class="-purple">Inches</span> &
          <span class="-purple">pixels.</span>
        </p>
        <p>
          In a past life, I was an indie mobile developer making mobile apps
          for iOS and Android and trying to build startup from scratch.<br />
        </p>
      </TextBlock>
    </SceneSection>
    <SceneSection id="early-days3">
      <TextBlock>
        <p>
          I've proudly partnered the starring<br />
          of some big Tech names such as
          <span class="-big -purple"
            ><em>Expo</em>, <em>Vercel</em>, GetStream,
            <em>Vox Implant</em></span
          >
          among many others...
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
