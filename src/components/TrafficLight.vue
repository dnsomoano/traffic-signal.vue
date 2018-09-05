<template>
    <section class="body">
        <section class="light-style">
            <button type="button" class="red-light" style={{ backgroundColor: `hsl(${{this.redLight.hue}},${{this.redLight.saturation}}%,${{this.redLight.lightness}}%)` }} v-on:click="changeColor">
            </button>
                <!-- <div class="red-light" v-on:click="changeColor" style={{ backgroundColor: `hsl(${{this.redLight.hue}},${{this.redLight.saturation}}%,${{this.redLight.lightness}}%)` }}/> -->
        </section>
        <section class="light-style">
            <button type="button" id="yellow-light"></button>
        </section>
        <section class="light-style">
            <button type="button" id="green-light"></button>
        </section>
    </section>
</template>

<script>
export default {
  name: "TrafficLight",
  /* declaration of key values in object */
  data: function() {
    return {
      redLight: {
        hue: 1,
        saturation: 0.5,
        lightness: 0.5
      },
      yellowLight: 0
    };
  },
  /* your methods start */
  methods: {
    changeColor: function() {
      console.log("Button was clicked");
      console.log(this.redLight.lightness);
      console.log(typeof this.redLight);
      event.target.value;
      /* Key values are called with this */
      this.redLight.lightness = 1.0;
      console.log(this.redLight.lightness);
    }
  }
};
</script>

<style scoped>
.light-style {
  /* display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center; */
}

/* Red light selectors */
.red-light {
  /* display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start; */
  height: 20em;
  width: 20em;
  border-radius: 10em;
  background-color: hsl(1, 50%, 50%);
}

/* yellow light selectors */
#yellow-light {
  /* display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start; */
  height: 20em;
  width: 20em;
  border-radius: 10em;
  background-color: yellow;
}

/* green light selectors */
#green-light {
  /* display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start; */
  height: 20em;
  width: 20em;
  border-radius: 10em;
  background-color: green;
  border-color: black;
}
</style>
