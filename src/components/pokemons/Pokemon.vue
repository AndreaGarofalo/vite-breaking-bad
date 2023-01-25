<script>
export default {
  name: "Pokemon",
  props: {
    name: String,
    image: String,
    number: Number,
    type1: String,
    type2: String,
  },
};
</script>

<template>
  <div class="col-2 m-2 poke-card">
    <figure>
      <img class="img-fluid" :src="image" />
    </figure>
    <figcaption>
      <p>{{ number }}</p>
      <h3>{{ name }}</h3>
      <p>{{ type1 }}</p>
      <p>{{ type2 }}</p>
    </figcaption>
  </div>
</template>

<style scoped lang="scss">
.poke-card {
  background-color: white;
  border-radius: 25px;
  overflow: hidden;
}
figcaption {
  text-align: center;
  p {
    margin-bottom: 0;
  }
}
</style>
