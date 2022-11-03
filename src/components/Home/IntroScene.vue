<template>
  <section class="scene-intro" id="intro">
    <div class="static-container">
      <h1 class="title">
        <span class="iuri">rokas</span>
        <span class="func">.com()</span>
      </h1>

      <TextBlock>
        <p class="-purple">Rokas Rudzianskas</p>
        <p class="-gray">Creative Full-Stack developer</p>
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
