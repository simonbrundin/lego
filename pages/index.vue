<template>
  <div class="container">
    <img class="lego-image" src="@/assets/lego_darth_wader.jpg" />
    <input v-model="setNumber" type="text" />
    <button @click="getLowestPrice(setNumber)">Hämta pris</button>
    {{ lowestPrice }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      lowestPrice: '0',
    };
  },
  computed: {
    setNumber() {
      return this.$store.state.setNumber;
    },
  },
  methods: {
    getLowestPrice(setNumber) {
      return fetch();
    },
  },
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.container > * {
  margin: 0 0 32px 0;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.lego-image {
  width: 200px;
}
</style>
