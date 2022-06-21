<template>
  <v-row justify="center" align="center">
    <v-col v-for="(item, index) in items" :key="index" cols="4">
      <Card :title="item.title" :paragraph="item.paragraph" :key="index+`${item.title}`" />
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "IndexPage",
  data: () => ({
    items: [
      {
        card1: {
          title: "1",
          paragraph: "p1",
        },
      },
      {
        card2: {
          title: "2",
          paragraph: "p2",
        },
      },
      {
        card2: {
          title: "3",
          paragraph: "p3",
        },
      },
    ],
  }),
};
</script>
