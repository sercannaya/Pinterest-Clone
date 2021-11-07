<template>
  <v-container>
      <stack :column-min-width="200" :gutter-width="10" :gutter-height="8">
        <stack-item v-for="(item, i) in items" :key="i">
          <image-card :url="item.url" :meta="{name: item.name, followers: item.followers, profileImageUrl: item.profileImageUrl}" />
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
          url: "https://images.unsplash.com/photo-1526048598645-62b31f82b8f5?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8dHVya2V5fGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Anya Feeney",
          followers: "248 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8dXNlcnxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1518084823714-2f59a7315a39?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTV8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Estelle Jordan",
          followers: "741 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8dXNlcnxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1531257240678-d5b1922e672d?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTF8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Federico Lugo",
          followers: "325 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1508214751196-bcfd4ca60f91?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8dXNlcnxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1579554370034-9aa1275e9c7b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjZ8fHR1cmtleXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60",
          name: "Iga Baker",
          followers: "128 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixid=MnwxMjA3fDB8MHxzZWFyY2h8OHx8dXNlcnxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1433838552652-f9a46b332c40?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Aarush Miranda",
          followers: "25 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTZ8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1567408773508-4e5da32afafd?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NTZ8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Tai Holt",
          followers: "157 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1532074205216-d0e1f4b87368?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjV8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1559554498-7a9eb7587782?ixid=MnwxMjA3fDB8MHxzZWFyY2h8N3x8dHVya2V5fGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Alessio Sandoval",
          followers: "90 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1587614382231-d1590f0039e7?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mjl8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1602941889598-3e7780b9a602?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTh8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Vicki Villanueva",
          followers: "862 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1489980557514-251d61e3eeb6?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MzR8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1596743220949-4a4b7d89cf01?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NjB8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Hawa Jenkins",
          followers: "146 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1484863137850-59afcfe05386?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NDR8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1582631608254-f75fdf938e19?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjV8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Issac Hartman",
          followers: "368 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1489424731084-a5d8b219a5bb?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NDh8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1602941800793-78c44baca4d8?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mjd8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Max Townsend",
          followers: "25 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1500648767791-00dcc994a43e?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTZ8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1598699924671-f3c536e35e8e?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MzR8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Arbaaz Bonner",
          followers: "157 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1532074205216-d0e1f4b87368?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjV8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1531584950177-ae3170a3d1c4?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mzl8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Aneesah Davidson",
          followers: "90 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1587614382231-d1590f0039e7?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mjl8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1596094657888-6e0a49139c1e?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NDV8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Raisa Jones",
          followers: "862 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1489980557514-251d61e3eeb6?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MzR8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1531255903991-ca714823bc1e?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NTF8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Monty Reynolds",
          followers: "146 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1484863137850-59afcfe05386?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NDR8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url: "https://images.unsplash.com/photo-1566682372561-2273e5226306?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NTN8fHR1cmtleXxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Clyde Ahmed",
          followers: "368 followers",
          profileImageUrl: "https://images.unsplash.com/photo-1489424731084-a5d8b219a5bb?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NDh8fHVzZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
      ],
    };
  },
};
</script>

<style>

</style>