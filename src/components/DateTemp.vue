<template>
  <div>
    <p>Current Date and Time: {{ currentDate }}</p>
    <p>Current Temperature in Paris, Ontario: {{ currentTemperature }}°C</p>
  </div>
</template>

<script>
import { format } from 'date-fns';

export default {
  data() {
    return {
      currentDate: '',
      currentTemperature: null
    };
  },
  created() {
    this.updateCurrentDate();
    this.fetchCurrentTemperature();
  },
  methods: {
    updateCurrentDate() {
      this.currentDate = format(new Date(), 'yyyy-MM-dd HH:mm:ss');
    },
    async fetchCurrentTemperature() {
      try {
        const response = await fetch(
          'https://api.openweathermap.org/data/2.5/weather?q=Paris,Ontario,CA&units=metric&appid=63629b5800e7396da95e57d15251ef28'
        );
        const data = await response.json();
        this.currentTemperature = data.main.temp;
      } catch (error) {
        console.error('Error fetching current temperature:', error);
      }
    }
  }
};
</script>
