<template>
  <div id="app">
    <InformerContainer>
      <InformerTemperature
        v-bind:temp-real="weather.temp"
        v-bind:temp-feel="weather.feel"
      ></InformerTemperature>
      <FlexBreak></FlexBreak>
      <InformerHumidity>{{ weather.humidity }}</InformerHumidity>
      <VerticalDivider></VerticalDivider>
      <InformerWind>{{ weather.wind }}</InformerWind>
    </InformerContainer>
  </div>
</template>

<script>
import InformerContainer from "./components/InformerContainer.vue";
import InformerTemperature from "./components/InformerTemperature.vue";
import InformerHumidity from "./components/InformerHumidity.vue";
import InformerWind from "./components/InformerWind.vue";
import VerticalDivider from "./components/VerticalDivider.vue";
import FlexBreak from "./components/FlexBreak.vue";

export default {
  name: "app",
  components: {
    InformerContainer,
    InformerTemperature,
    InformerHumidity,
    InformerWind,
    VerticalDivider,
    FlexBreak
  },
  data() {
    return {
      weather: {}
    };
  },
  methods: {
    updWeather() {
      this.axios
        .get("http://188.225.47.187/api/weather/json.php")
        .then(response => {
          this.weather = response.data;
        });
    }
  },
  mounted() {
    this.updWeather();
  }
};
</script>
