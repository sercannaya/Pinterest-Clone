<template>
  <v-container>
      <div>Home Page</div>
      <stack :column-min-width="200" :gutter-width="10" :gutter-height="8">
        <stack-item v-for="(item, i) in items" :key="i">
          <image-card :url="item.url" :meta="{name: item.name, occupation: item.occupation, profileImageUrl: item.profileImageUrl}" />
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
          url: "https://images.unsplash.com/photo-1544735716-392fe2489ffa?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8bmVwYWx8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Name Surname",
          occupation: "Sample Occupation",
          profileImageUrl: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8dXNlcnxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1554710869-95f3df6a3197?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8bmVwYWx8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Name Surname",
          occupation: "Sample Occupation",
          profileImageUrl: "https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8dXNlcnxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1571401835393-8c5f35328320?ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8bmVwYWx8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Name Surname",
          occupation: "Sample Occupation",
          profileImageUrl: "https://images.unsplash.com/photo-1508214751196-bcfd4ca60f91?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8dXNlcnxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1512036594830-51cea3a8df78?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTF8fG5lcGFsfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Name Surname",
          occupation: "Sample Occupation",
          profileImageUrl: "https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixid=MnwxMjA3fDB8MHxzZWFyY2h8OHx8dXNlcnxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1533130061792-64b345e4a833?ixid=MnwxMjA3fDB8MHxzZWFyY2h8OXx8bmVwYWx8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Name Surname",
          occupation: "Sample Occupation",
          profileImageUrl: "https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTZ8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1616392327822-626a27e24c2e?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTV8fG5lcGFsfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Name Surname",
          occupation: "Sample Occupation",
          profileImageUrl: "https://images.unsplash.com/photo-1532074205216-d0e1f4b87368?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjV8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1545662618-66de187bbf69?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTR8fG5lcGFsfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Name Surname",
          occupation: "Sample Occupation",
          profileImageUrl: "https://images.unsplash.com/photo-1587614382231-d1590f0039e7?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mjl8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1585597800810-07a63ea8e983?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTd8fG5lcGFsfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Name Surname",
          occupation: "Sample Occupation",
          profileImageUrl: "https://images.unsplash.com/photo-1489980557514-251d61e3eeb6?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MzR8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1511215579272-6192432f83bc?ixid=MnwxMjA3fDB8MHxzZWFyY2h8OHx8bmVwYWx8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Name Surname",
          occupation: "Sample Occupation",
          profileImageUrl: "https://images.unsplash.com/photo-1484863137850-59afcfe05386?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NDR8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1550642249-6e5605421172?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8bmVwYWx8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Name Surname",
          occupation: "Sample Occupation",
          profileImageUrl: "https://images.unsplash.com/photo-1489424731084-a5d8b219a5bb?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NDh8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
      ],
    };
  },
};
</script>

<style>

</style>