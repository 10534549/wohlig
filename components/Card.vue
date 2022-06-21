<template>
  <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-card-text>
      <p class="text-h4 text--primary">{{ this.title }}</p>
      <div class="text--primary">{{ this.paragraph }}</div>
    </v-card-text>
    <v-card-actions>
      <v-btn
        text
        color="teal accent-4"
        @click="reveal = true"
      >
        Learn More
      </v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
  export default {
    props: ["title", "paragraph"],
    data: () => ({
      reveal: false,
    }),
    watch: {
        title: function (newVal) {
            console.log(newVal);
        }
    }
  }
</script>
<style>
.v-card--reveal {
  bottom: 0;
  opacity: 1 !important;
  position: absolute;
  width: 100%;
}
</style>