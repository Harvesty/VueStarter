<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div>{{info}}</div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'About',
  data() {
    return {
      info: {}
    };
  },
  mounted() {
    axios
      .get("api/weatherforecast")
      .then(response => (this.info = response.data));
  }
}
</script>
