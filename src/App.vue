<template>
  <div id="app">
    <InformerContainer>
      <InformerTemperature temp-real="10" temp-feel="7"></InformerTemperature>
      <FlexBreak></FlexBreak>
      <InformerHumidity>12</InformerHumidity>
      <VerticalDivider></VerticalDivider>
      <InformerWind>13</InformerWind>
    </InformerContainer>
  </div>
</template>

<script>
import InformerContainer from './components/InformerContainer.vue'
import InformerTemperature from './components/InformerTemperature.vue'
import InformerHumidity from './components/InformerHumidity.vue'
import InformerWind from './components/InformerWind.vue'
import VerticalDivider from './components/VerticalDivider.vue'
import FlexBreak from './components/FlexBreak.vue'

export default {
  name: 'app',
  components: {
    InformerContainer,
    InformerTemperature,
    InformerHumidity,
    InformerWind,
    VerticalDivider,
    FlexBreak
  },
  
}
</script>
