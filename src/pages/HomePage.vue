<template>
  <v-container>
      <div>Home Page</div>
      <stack :column-min-width="320" :gutter-width="8" :gutter-height="8">
        <stack-item v-for="i in 8" :key="i">
          <image-card />
        </stack-item>
      </stack>
  </v-container>
</template>

<script>
import { Stack, StackItem } from 'vue-stack-grid';
import ImageCard from "../components/ImageCard.vue";

export default {
  components: { Stack, StackItem, ImageCard },
  data() {
    return {
      items: [
        {
          someContent: "hello",
        },
      ],
    };
  },
};
</script>

<style>

</style>